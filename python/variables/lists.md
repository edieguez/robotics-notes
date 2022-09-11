# Python lists

Lists in Python can be [sliced](../slices.md)

> All the methods that accept an index can also accept a **negative index** where `-1` is the last element in the list and so on

## Replace elements

```python
hex_letters = ['10', '11', 'C', 'D', '14', '15']

# Replace with positive indexes
hex_letters[0] = 'A'
hex_letters[1] = 'B'

# Replace with negative indexes
hex_letters[-2] = 'E'
hex_letters[-1] = 'F'

# hex_letters = ['A', 'B', 'C', 'D', 'E', 'F']
```

## Insert elements

```python
letters = ['a', 'c']
letters.insert(1, 'b')

print(letters)
```

> **Output**
> ['a', 'b', 'c']

## Delete elements

```python
letters = ['a', '0', '1', 'b', '2', 'c']

# Delete elements with positive index
del letters[1]

# Delete elements with negative index
del letters[-2]
del letters[-3]

# letters = ['a', 'b', 'c']
```

## Remove method

> Removes an element based on the received value instead of using an index. It **only removes the first ocurrence** of the value.

```python
letters = ['a', 'b', 'c', 'b']
letters.remove('b')

print(letters)
```

> **Output**
> ['a', 'c', 'b']

## Pop elements

```python
letters = ['a', 'b', 'c']

print(letters.pop(1))

for times in range(len(letters)):
    print(letters.pop())

print(letters)
```

> **Output**
> b
> c
> a
> []

## Sorting a list

```python
numbers = [5, 3, 1, 2, 4]
numbers.sort()

print(numbers)

numbers.sort(reverse=True)
print(numbers)
```

> **Output**
> [1, 2, 3, 4, 5]
> [5, 4, 3, 2, 1]

## Sorting a list using the `sorted()` method

Is similar to the `list.sort()` method but it **does not affect the original list**

```python
numbers = [5, 3, 1, 2, 4]

print(sorted(numbers))
print(numbers)
```

> **Output**
> [1, 2, 3, 4, 5]
> [5, 3, 1, 2, 4]

## Reversing a list

This method **affects the original list**

```python
numbers = [1, 2, 3, 4, 5]
numbers.reverse()

print(numbers)
```

> **Output**
> [5, 4, 3, 2, 1]
