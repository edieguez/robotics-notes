# Aggregation pipelines

## `$group` example

```javascript
db.inventory.aggregate({
  $group: {
    _id: '$source',
    count: {$sum: 1},
    items: {$push: '$name'},
    avg_price: {$avg: '$price'}
  }
}).sort({avg_price: 1})
```

## `$unwind` example

> The first `$match` is to filter out all the elements that are not 'Purple' before appliying `$unwind`.
> It has to be specified twice, otherwise `$unwind` will output all the variations ignoring the filter

```javascript
db.inventory.aggregate([
  {
    $match: {
      'variations.variation': 'Purple'
    }
  },
  {
    $unwind: '$variations'
  },
  {
    $match: {
      'variations.variation': 'Purple'
    }
  }
])
```

## `$out` example

> Saves the the query's output to `sample_data.purple` collection.
> It overrides the target collection

```javascript
db.inventory.aggregate([
  {
    $match: {
      'variations.variation': 'Purple'
    }
  },
  {
    $unwind: '$variations'
  },
  {
    $match: {
      'variations.variation': 'Purple'
    }
  },
  {
    $out: {
      db: 'sample_data',
      coll: 'purple'
    }
  }
])
```

## $merge example

```javascript
db.inventory.aggregate([
  {
    $match: {
      'variations.variation': 'Purple'
    }
  },
  {
    $unwind: '$variations'
  },
  {
    $match: {
      'variations.variation': 'Purple'
    }
  },
  {
    $merge: {
      into: 'purple',
      on: '_id',
      whenMatched: 'keepExisting',
      whenNotMatched: 'insert'
    }
  }
])
```
