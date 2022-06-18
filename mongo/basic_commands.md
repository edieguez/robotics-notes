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

# updates the entire document. The upsert part is optional
db.$collection.updateOne(
    {
        _id: ObjectId("62adfcd60ef724af7e477f27")
    },
    $set: {
        name: "Seiga",
        lastname: "Kaku"
    },
    {
        upsert: true
    }
)
```
