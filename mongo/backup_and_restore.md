# Backup and restore Mongo collections

## Backup

```shell
# Backup in BSON format. The output is stored in a directory and also contains metadata
mongodump --uri "mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>"

# Backup in JSON format
mongoexport --uri="mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>" --collection=<collection_name> --out=<filename>.json
```

## Restore

```shell
# Restore backups in BSON format
mongorestore --uri "mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>"  --drop <dump_directory>

# Restore backups in JSON and BSON formats
mongoimport --uri="mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>" --drop <filename>.json
```
