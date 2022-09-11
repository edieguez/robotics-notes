# Slices

Slices can work with `str`, `list`, `tuple` or any `iterable`. It returns a `list`

Is the action of taking sublists from a bigger `iterable`

``` python
list_ = ['a', 'b', 'c', 'd', 'e']

# invert list_
list_[::-1]

# ['c', 'd', 'e']
list_[2:len(list_)]

# exclude the last two elements
# ['a', 'b', 'c']
list_[:-2]
```

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
