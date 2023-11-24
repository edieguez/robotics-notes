# Upsert

Is a combination of `update` and `insert` operations. If the document exists, it will be updated, otherwise it will be inserted. For this operation to succeed, ==the field we are updating **MUST** exist==. Otherwise, the operation will fail.

```json
curl -X POST "https://127.0.0.1:9200/products/_update/oSoCAowB9JgqE6xFoeh6?pretty" -H 'Content-Type: application/json' -d'
{
  "script": {
    "source": "ctx._source.price += 100"
  },
  "upsert": {
    "name": "iPad pro",
    "price": "1000",
    "currency": "USD",
    "in_stock": 3
  },
}
'
```
