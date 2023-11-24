# Scripted updates

You can write more complex logic when updating a document using the `script` parameter. The script can be written in `painless` or `expression` language.

```bash
# Apply 25% discount to the price
curl -X POST "https://127.0.0.1:9200/products/_update/oSoCAowB9JgqE6xFoeh6?pretty" -H 'Content-Type: application/json' -d'
{
  "script": {
    "source": "ctx._source.price *= 0.75"
  }
}
'
```

It also accepts a `params` object that can be used to pass parameters to the script.

```bash
# Apply 25% discount to the price
curl -X POST "https://127.0.0.1:9200/products/_update/oSoCAowB9JgqE6xFoeh6?pretty" -H 'Content-Type: application/json' -d'
{
  "script": {
    "source": "ctx._source.price *= params.discount",
    "params": {
      "discount": 0.75
    }
  }
}
'
```
