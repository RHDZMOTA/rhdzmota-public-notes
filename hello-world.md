## Hello, World!


This blogpost some simple examples of hello-world programs.

### Python

You can easily print a hello-world in Python by directly adding the following on a `main.py` file.

```python=
print("Hello, World!")
```

Execution:

```commandline
$ python main.py
```

Adding the following validation prevents printing the hello-world call when using `main` as a module:

```python=

if __name__ == "__main__":
    print("Hello, World!")

```