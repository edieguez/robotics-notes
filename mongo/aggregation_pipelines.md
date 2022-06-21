# Aggregation pipelines

## Group example

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
