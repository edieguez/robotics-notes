# Amazon Athena

**Serverless** query service to analyze data store in [S3](s3.md). Uses **standard SQL to query files** (build in Presto)

Supports the following file formats

- CSV
- JSON
- Avro
- Parquet

It is commonly used with `Amazon Quicksight` for reporting/dashboards

## Performance improvements

- Use **columnar data** (allows less scanning)
  - `Aparche Parquet` or `OCR` is recommended
  - Use `Glue` to convert your data to `Parquet` or `ORC`
- **Compress data** for smaller retrievals
- **Partition datasets** in S3 for easy querying on virtual columns
- **Use larger files (> 128 MB)** to minimize overhead

## Federated queries

Allows you to **run SQL across data stored in relational, non-relational, object and custom data sources** (AWS or on premises). Uses `data source connectors` that run on `Lambda`. It supports the following data sources (not an exhaustive list)

- ElasticCache
- DocumentDB
- DynamoDB
- Redshift
- Aurora
- SQL server
- MySQL
- CloudWatch logs
- DynamoDB
- RDS

It stores the results back in `S3` for further analysis
