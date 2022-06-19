# Logical operators

- $and
- $or
- $nor
- $not

## $and example

```javascript
db.users.find({
  $and: [
    { name: 'John' },
    { age: { $gt: 18 } }
  ]
})
```

## $or example

```javascript
db.users.find({
  $or: [
    { name: 'John' },
    { age: { $gt: 18 } }
  ]
})
```

## $nor example

```javascript
db.users.find({
  $nor: [
    { name: 'John' },
    { age: { $gt: 18 } }
  ]
})
```

## $not example

```javascript
db.users.find({
  $not: {
    { name: 'John' },
    { age: { $gt: 18 } }
  }
})
```
