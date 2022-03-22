# Slices

Slices can work with `str`, `list` or any `iterable`

`string[:]`
`string[:end]`
`string[start:]`
`string[start:end:step]`

`start` Optional and inclusive. Default 0
`end` Optional and exclusive. Defaults to the end of the string
`step` Optional. Default 1. If negative, iterates in `reverse`

```python
string = 'Hello world'

hello = string[0:5]
world = string[6:11]

print(f'{hello} {world}') # Hello world
print(string[::-1])       # dlrow olleH

```
