# Variable unpacking

## [List](variables/lists.md)/tuple unpacking

``` python
def print_pairs(x, y):
    print(x, y)


pairs = (('a', 'b'), ('A', 'B'))

# Variable unpacking
print_pairs(*pairs)
```

> **Output**
> ('a', 'b') ('A', 'B')

## Dictionary unpacking

In a dictionary the keys in the `dict` **MUST** match the argument names received by the function

``` python
def print_pairs(first, second):
    print(first, second)


pairs = {
    'first': ('a', 'b'),
    'second': ('A', 'B')
}

# Variable unpacking
print_pairs(**pairs)
```

> **Output**
> ('a', 'b') ('A', 'B')
