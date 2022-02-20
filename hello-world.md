## Coding a simple 'hello world' program


This blogpost contains some simple examples of hello-world programs in different languages:
* `python`
* TBD

### Python

You can easily print a hello-world in Python by directly adding the following on a `main.py` file.

```python=
print("Hello, World!")
```

Execution:

```commandline
$ python main.py
```

#### Preventing side-effects

You may have notice that the usage of the `main.py` python script as a module also triggers the hello-world statement.

```python=
import main  # This unintentonally prints the 'Hello,  World!' string

# ...
```


Adding the following validation prevents printing the hello-world side-effect on imports:

```python=

if __name__ == "__main__":
    print("Hello, World!")

```

Notice that the code still prints the 'Hello, World!' when running:

```commandline
python main.py
```

#### Reusability

By now, we know how to execute the hello-world program and avoid any side-effects when using it as a module. Let's refactor the code so that we can re-utilize the hello-world implementation on different appliccations:


```python=


def hello_world():
    print("Hello, World!")


if __name__ == "__main__":
    hello_world()
    
```

By implementing the `hello_world` function, we can now use this implementation in different scripts by importing the definition:

```python=
from main import hello_world  # Import without side-effects

# ...
```


#### Parametrization

We can parametrize the `hello_world` function so that we can select an arbitrary name.

```python=

def hello_world(name: str):
    print(f"Hello, {name}!")


if __name__ == "__main__":
    hello_world(name="World")

```

#### Default parameters

We can now define a default parameter to make the argument optional.


```python=
from typing import Optional


def hello_world(name: Optional[str] = None):
    name = name or "World"
    print(f"Hello, {name}!")
    
if __name__ == "__main__":
    hello_world()

```


#### Default Configurable parameters


```python=
import os
from typing import Optional


DEFAULT_WORLD = os.environ.get(
    "DEFAULT_WORLD",
    default="World"
)


def hello_world(name: Optional[str] = None):
    name = name or DEFAULT_WORLD
    print(f"Hello, {name}!")
    
if __name__ == "__main__":
    hello_world()

```


This allows us to change the default argument value:

```commandline
$ python main.py
```

```commandline
$ DEFAULT_WORLS=example python main.py
```

#### Commandline arguments

```python=
import argparse
import os
from typing import Optional


DEFAULT_WORLD = os.environ.get(
    "DEFAULT_WORLD",
    default="World"
)


def hello_world(name: Optional[str] = None):
    name = name or DEFAULT_WORLD
    print(f"Hello, {name}!")
    
    
if __name__ == "__main__":
    # Instance argument parser, configure and retrieve arguments
    parser = argparse.ArgumentParser(description="Hello World Program")
    parser.add_argument("--world", default=DEFAULT_WORLD)
    args = parser.parse_args()
    # Execute hello-world
    hello_world(name=args.world)

```
