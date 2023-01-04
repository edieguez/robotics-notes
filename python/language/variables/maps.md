# Python maps

> Starting in Python 3.7, looping through a dictionary returns the items in the same order they were inserted

## Create a map

```python
heian_alien = {
    'name': 'undefined',
    'color': 'black',
    'points': 5
}
```

## Replace `value`

```python
heian_alien['name'] = 'Nue Houjuu'
```

## Add new `key`, `value` pair

```python
heian_alien['x_position'] = 12
heian_alien['y_position'] = 0
```

## Delete `key`, `value` pair

```python
del heian_alien['points']
```

## Get or default

```python
print(heian_alien.get('points')) # None
print(heian_alien.get('points', 'Not found'))
```

## `key` iteration

```python
for key in heian_alien.keys():
    print(f'{key}: {heian_alien[key]}')

for key in heian_alien:
    print(f'{key}: {heian_alien[key]}')
```

## `value` iteration

```python
for value in heian_alien.values():
    print(f'{value}')
```

## `key`, `value` Iteration

```python
for key, value in heian_alien.items():
    print(f'{key}: {value}')
```
