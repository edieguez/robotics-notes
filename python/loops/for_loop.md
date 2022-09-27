# For loop

- `iterable` variable can be any Python [iterable](https://docs.python.org/3/glossary.html#term-iterable). Including generators.
- An additional [`else`](else.md) clause is accepted in this loop
- A *compressed* version of this loop can be found in [list comprehensions](comprehension.md)

## For each

```python
iterable = '0123456789'

for element in iterable:
    print(element)
```

## For with index

```python
iterable = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

for index in range(10):
    print(iterable[index])
```

## For with index and step

```python
iterable = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

for index in range(1, 10, 2): # Print only odd numbers
    print(iterable[index])
```

## For with index using `enumerate`

``` python
iterable = 'abcdefghijklmnopqrstuvwxyz'

# start argument is optional
for index, element in enumerate(iterable, start=1):
    print(f'index: {index}, element: {element}')
```
