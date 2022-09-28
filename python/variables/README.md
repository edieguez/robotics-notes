# Basic data types

- Numbers: `1`, `10`, `999`
- Floating point numbers: `1.5`, `3.1416`
- Strings: `"hello world"`, `'Python'`
- [Boolean](boolean.md): `True`, `False`
      - In an integer context, boolean literals take the value of 1 and 0 respectively
- [Lists](lists.md)
- Tuples: similar to `list` but immutable
- [Maps](maps.md)

## Converting basic types

### String to integer

```python
number_as_string = '10'
number_as_integer = int(number_as_string)
```

### Float string to integer

```python
float_as_string = '1.5'
float_as_integer = int(float_as_string)

>>> ValueError: invalid literal for int() with base 10: '1.5'
```

### Integer to float

```python
integer_number = 10
float_number = float(integer)  # 10.0
```
