# Basic commands

```shell
# show databases
show dbs

# switch to $database
use $database

# show collections
show collections

# insert $JSON into $collection
db.$collection.insert($JSON)

# insert MANY registries into $collection
db.$collection.insertMany($JSON)

# updates the entire document
db.$collection.update(
    {
        _id: "123abc"
    },
    {
        name: "Seiga",
        lastname: "Kaku"
    },
    {
        upsert: true
    }
)
```
