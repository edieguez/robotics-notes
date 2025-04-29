# Elastic Map Reduce (EMR)

Helps creating `Hadoop clusters (big data)` to analyze and process large amounts of data. It **can be used for data processing**, **machine learning**, **web indexing**, and more.

It comes bundled with

- Apache Spark
- HBase
- Presto
- Flink

It is a fully managed service that allows you to focus on your data and analytics, not on managing the infrastructure. It also supports `spot instances` to reduce costs

## Node types

> Can have **long-running cluster** or **transient (temporary) cluster**

- `Master node` manage the cluster, coordinate, manage health (**long running**)
- `Core node` run tasks and store data (**long running**)
- `Task node` run tasks but do not store data (**short running and also optional**)

## Purchasing options

### On-demand

- Reliable
- Predictable
- Won't be terminated

### Reserved

- **1-3 years** commitment
- **Cost savings**
- EMR will use it automatically if available

### Spot instances

- Cheaper, in fact, **the cheapest option**
- **Can be terminated at any time**
- Less reliable
