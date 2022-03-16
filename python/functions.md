# Functions

Python is an interpreted language. For that reason functions **must be defined before** using them. Optionally, functions can return a value using the `return` keyword.

## Syntax

### Simple

```python
def function_name():
    pass
```

### With parameters

```python
def function_name(param_a, param_b):
    pass
```

### Parameters with types

Introduced in Python 3.5 ([PEP 484](https://peps.python.org/pep-0484/))

```Python
def function_name(param_a: list, param_b: str) -> int:
    return 42
```
