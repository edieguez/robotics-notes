# [Exceptions](https://docs.python.org/3/tutorial/errors.html#handling-exceptions)

In Python (unlike other languages) we don't throw an exception. We `raise` exceptions

``` python
raise Exception('Exception message')
```

## Basic construct

``` python
try:
    ...
except (Exception_A, Exception_B) as e:
    ...
except (Exception_C, Exception_D), e:
    ...
except Exception_E as e:
    ...
except Exception_F:
    ...
except:
    ...
else:
    ...
finally
    ...
```

### `try`

This block includes the code that can raise an exception

### `except`

- A single `try`  can have multiple `except`  blocks to catch multiple kinds of exceptions.
- An `except`  without any specific exception can be added to catch all the exceptions

### `else`

This is an optional clause. If no exception is raised, this code block is executed. It is also executed **before** the `finally`  block

### `finally`

This code block is executed no matter if an exception was raised or not. It will be **always** executed at the end even if there's a `return`, `break` or `continue` statement in the `try`, `except`  or `else`  blocks

## Considerations

- The wildcard `except` clause is equivalent to `except Exception`. It will catch almost all the exceptions. The exceptions based on `BaseException` won't be affected and need to be explicitly handled
- At least one `except` or `finaly` clause is required in the `try` statement
