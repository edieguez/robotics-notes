# Amazon Managed Streaming for Apache Kafka (MSK)

It is an alternative for Amazon Kinesis. It uses Apache Kafka as the underlying technology to build a scalable, durable, and highly available streaming platform. **Data is stored in EBS volumes for as long as you want**

| Kinesis Data Streams        | Amazon MSK                                     |
| --------------------------- | ---------------------------------------------- |
| 1 MB message size limit     | 1 MB default, configure for higher (ex: 10 MB) |
| Data Streams with Shards    | Kafka topics with Partitions                   |
| Shard splitting and merging | Can only add partitions to a topics            |
| TLS in-flight encryption    | PLAINTEXT or TLS in-flight encryption          |
| KMS at-rest encryption      | KMS at-rest encryption                         |

## Consumers

- Kinesis Data Analytics for Apache Flink
- AWS Glue
- Apache Spark Streaming
- Lambda
- Applications running on
  - Amazon EC2
  - ECS
  - EKS
