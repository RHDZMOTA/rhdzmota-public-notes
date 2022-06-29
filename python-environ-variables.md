
You can easily retrieve environ variables with python via the `os` module:

```python=
import os

# Fails if VAR_1 is not defined
VAR_1 = os.envion["VAR_1"]

# Defaults to `None` if `VAR_2` is not defined.
VAR_2 = os.envion.get("VAR_2")

# Defaults to `value` if `VAR_3` is not defined.
VAR_3 = os.envion.get(
    "VAR_3",
    default="value",
) 
```

The following abstraction can standardize the common use-cases:

```python=
import os
from typing import Callable, Optional, Union, TypeVar

T = TypeVar("T")

def get_environ_variable(
        name: str,
        default: Optional[str] = None,
        enforce: bool = False,
        apply: Optional[Callable[[Optional[str]], T]] = None,
) -> Optional[Union[Optional[str], T]]:
    return (apply or (lambda x: x))(
        os.environ.get(name, default=default) if not enforce else
        os.environ.get(name) or (lambda: (_ for _ in ())
            .throw(ValueError(f"Missing environ variable: {name}")))()
    )
    
```

Usage example: 

* `get_environ_variable(name="VAR_1")` - Get the `VAR_1` environ variable; fallback to `None`.
* `get_environ_variable(name="VAR_2", default="value")` - Get the `VAR_2` environ variable; fallback to `value`.
* `get_environ_variable(name="VAR_3", enforce=True)` - Get the `VAR_3` environ variable; fail if not found.

![](https://hackmd.io/_uploads/r1q8Pr59q.png)
