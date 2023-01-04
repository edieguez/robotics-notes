# List comprehension

``` python
# Get the powers of 2 of the numbers between 0 and 10
#    output      collection       condition
l = [x  ** 2 for x in range(11) if x % 2 == 0]

print(l)
```

> **Output**
> [0, 4, 16, 36, 64, 100]

- `output` do this
- `collection` for this collection
- `condition` in this situation. This part is optional
