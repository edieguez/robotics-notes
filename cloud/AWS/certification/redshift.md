# Redshift

Is based on `PostgreSQL` but it is not used for [OLTP](../../../wiki/dictionary/oltp.md). It supports [OLAP](../../../wiki/dictionary/olap.md) (analytics and data warehousing).

It has **10x better performance than other data warehouses** and can scale to **PetaBytes of data**. It is a **columnar storage** database that is optimized for **read-heavy workloads**.

Offers integration with BI tools like `Amazon Quicksight` and `Tableau`.

## VS Athena

- **Faster queries, joins and aggregations thanks to indexes**
- You need to provision your cluster since **it is not serverless**

## Snapshots and disaster recovery (DR)

- Multi AZ mode for some clusters
- Point-in-time backups stored internally in S3
- **Incremental snapshots** only what has changed is saved
- **Restore snapshots to a new cluster**
- **Automated backups** every 8 hours, every 5 GB or on schedule
  - Retention can be set to 1 to 35 days
- **Manual backups** are retained until you delete them
- **Can be configured to automatically copy snapshots to another region**

## Redshift Spectrum

- **Query data in S3** without loading it into Redshift
- **Must have Redshift cluster** to start the query
- Query processing is provided by **Redshift Spectrum nodes**
