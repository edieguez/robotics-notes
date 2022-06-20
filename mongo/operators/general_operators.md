# General operators

- $exists
- $set
- $unset
- $inc
- $mul
- $max
- $min
- $all
- $elemMatch

## $exists example

```javascript
db.users.find({
  name: { $exists: true }
})
```

## $set example

```javascript
db.$collection.updateOne(
    {
        _id: ObjectId('62adfcd60ef724af7e477f27')
    },
    $set: {
        name: 'Seiga',
        lastname: 'Kaku'
    },
    {
        upsert: true
    }
)
```

## $unset example

Removes the field from the document.
You must specify a value just for the sake of syntax. The value is ignored.

```javascript
db.$collection.updateOne(
    {
        _id: ObjectId('62adfcd60ef724af7e477f27')
    },
    $unset: {
        name: '
    }
)
```

## $all example

```javascript
db.movies.find({
  genres: { $all:
    ['Horror', 'Drama']
  }
})
```

## $elemMatch example

```javascript
db.inventory.find({
  variations: {
    $elemMatch: {
      variation: 'Blue',
      quantity: {$gt: 0}
    }
  }
})
```
