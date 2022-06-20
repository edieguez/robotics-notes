# Logical operators

1. $and
2. $or
3. $nor
4. $not

## $and example

```javascript
db.inventory.find({
  $and: [
    {name: 'BMW'},
    {year: 1992}
  ]
})
```

## $or example

```javascript
db.inventory.find({
  $or: [
    {name: 'BMW'},
    {year: 1992}
  ]
})
```

## $nor example

```javascript
db.inventory.find({
  $nor: [
    {name: 'BMW'},
    {year: 1992}
  ]
})
```

## $not example

```javascript
db.inventory.find({
  $and: [
    {
      name: {
        $not: {
          $eq: 'BMW'
        }
      }
    },
    {
      year: {
        $not: {
          $eq: 1992
        }
      }
    }
  ]
})
```
