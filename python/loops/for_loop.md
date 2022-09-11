# For loop

`iterable` variable can be any Python iterable. Including generators

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
