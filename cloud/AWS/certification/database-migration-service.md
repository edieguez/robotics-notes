# Database Migration Service (DMS)

Migration service that helps you migrate databases to AWS quickly and securely. The **source database remains fully operational during the migration**, minimizing downtime to applications that rely on the database

It offers `Continuous Data Replication` and `Change Data Capture` capabilities. It order to perform a migration, you need to create a `replication instance` and `endpoints` for the source and target databases. In practice, that means you need to **spin up a EC2 instance to perform the replication tasks**

## Schema Conversion Tool (SCT)

Helps you convert the schema of your source database to a format compatible with the target database. It also converts the code of your stored procedures, functions, and triggers to the target database's format

## Supported databases

- On-premises and EC2 instances
  - Oracle
  - MS SQL Server
  - MySQL
  - MariaDB
  - PostgreSQL
  - MongoDB
  - SAP
  - DB2
- Azure SQL Database
- RDS
  - All, including Aurora
- Amazon S3
- DocumentDB

## Target databases

- On-premises and EC2 instances
  - Oracle
  - MS SQL Server
  - MySQL
  - MariaDB
  - PostgreSQL
  - SAP
- Amazon RDS
- Redshift
- DynamoDB
- S3
- OpenSearch Service
- Kinesis Data Streams
- Apache Kafka
- DocumentDB and Amazon Neptune
- Redis and Babelfish
