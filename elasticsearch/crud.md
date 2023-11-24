# Basic CRUD operations

Elasticsearch uses a REST API to allow the user to interact with the database. This means that the user can use the HTTP methods GET, POST, PUT, DELETE, etc. to perform operations on the database

> Using CURL you may need to authenticate using the `-u` flag and allow insecure connections using the `-k` flag
>
> ```bash
> curl -u $username:$password -k ...
> ```

## Create collection

To create a new collection, we can use the `PUT` method

```bash
curl -X PUT "https://127.0.0.1:9200/products?pretty"
```

The response should look like this:

```json
{
  "acknowledged": true,
  "shards_acknowledged": true,
  "index": "products"
}
```

## Create document

To create a new document in the database, we can use the `PUT` method

```bash
curl -X POST "https://127.0.0.1:9200/products/_doc?pretty" -H 'Content-Type: application/json' -d'
{
  "name": "computer",
  "price": 1000,
  "currency": "USD"
}
'
```

The response should look like this:

```json
{
  "_index": "products",
  "_id": "oSoCAowB9JgqE6xFoeh6",
  "_version": 1,
  "result": "created",
  "_shards": {
    "total": 2,
    "successful": 1,
    "failed": 0
  },
  "_seq_no": 0,
  "_primary_term": 1
}
```

> Take note of the `_id` field. It will be used in other operations like `GET`, `DELETE`, `PUT`, etc.

## Update document

To update a document, we can use the `PUT` method

```bash
curl -X PUT "https://127.0.0.1:9200/products/_doc/oSoCAowB9JgqE6xFoeh6?pretty" -H 'Content-Type: application/json' -d'
{
  "name": "Macbook pro",
  "price": 1400,
  "currency": "USD"
}
'
```

The response should look like this:

```json
{
  "_index": "products",
  "_id": "oSoCAowB9JgqE6xFoeh6",
  "_version": 2,
  "result": "updated",
  "_shards": {
    "total": 2,
    "successful": 1,
    "failed": 0
  },
  "_seq_no": 1,
  "_primary_term": 1
}
```

## Partially update document

To partially update a document, we can use the `POST` method. Notice that we are using the `_update` endpoint. ==If the key does not exist, it will be created==

```bash
curl -X POST "https://127.0.0.1:9200/products/_update/oSoCAowB9JgqE6xFoeh6?pretty" -H 'Content-Type: application/json' -d'
{
  "doc": {
    "price": 1500
  }
}
'
```

## Get document

Using the `_id` of the document, we can get the document using the `GET` method

```bash
curl -X GET "https://127.0.0.1:9200/products/_doc/oSoCAowB9JgqE6xFoeh6?pretty"
```

You will get the updated version of the document

```json
{
  "_index": "products",
  "_id": "oSoCAowB9JgqE6xFoeh6",
  "_version": 2,
  "_seq_no": 1,
  "_primary_term": 1,
  "found": true,
  "_source": {
    "name": "Macbook pro",
    "price": 1500,
    "currency": "USD"
  }
}
```

> To get all the documents you can use
>
> ```bash
> curl -X GET "https://127.0.0.1:9200/products/_search?pretty"
> ```

## Delete document

Using the `_id` of the document, we can delete the document using the `DELETE` method

```bash
curl -X DELETE "https://127.0.0.1:9200/products/_doc/oSoCAowB9JgqE6xFoeh6?pretty"
```

The response should look like this:

```json
{
  "_index": "products",
  "_id": "oSoCAowB9JgqE6xFoeh6",
  "_version": 3,
  "result": "deleted",
  "_shards": {
    "total": 2,
    "successful": 1,
    "failed": 0
  },
  "_seq_no": 2,
  "_primary_term": 1
}
```
