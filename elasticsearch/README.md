# Elastic stack

Is a set of tools for collecting, storing and visualizing data. It is composed of

- `Elasticsearch`
- `Logstash`
- `Kibana`
- `Beats`
- `X-Pack`

It was originally known as the **ELK stack** (`Elasticsearch`, `Logstash`, `Kibana`). When Beats data shippers and X-Pack were added, the term "**ELK stack**" became inaccurate, so the community decided to rename it to the Elastic stack.

Some concepts that need to be understood before using the Elastic stack are

- `nodes` are instances of Elasticsearch running in a single JVM
- `cluster` is a collection of one or more nodes that together holds your entire data and provides federated indexing and search capabilities across all nodes
- `index` is a collection of documents that have somewhat similar characteristics
- `document` is a basic unit of information that can be indexed
- `shards` are the containers for your data. They are how Elasticsearch distributes data around your cluster
- `replicas` are copies of your shards. Replicas provide high availability in case a shard/node fails. Replicas are also used to scale out read operations
- `mapping` is like a database schema. It describes the fields in the documents along with their datatypes, and how they should be indexed and stored by `Lucene`
- `field` is a single piece of data in a document. Fields are the basic units of data in Elasticsearch. A field is roughly analogous to a column in a relational database
- `type` is a logical category/partition of your index whose semantics is completely up to you. In general, a type is defined for documents that have a set of common fields
- `query` is a way to search and filter documents in Elasticsearch
- `aggregation` is a way to group and extract statistics from your data
- `pipeline` is a way to transform documents before indexing

## Elasticsearch

Is a distributed, RESTful search and analytics engine capable of solving a growing number of use cases. As the heart of the Elastic Stack, it centrally stores your data so you can discover the expected and uncover the unexpected.

## Logstash

Is a dynamic data collection pipeline with an extensible plugin ecosystem and strong Elasticsearch synergy. It has three kinds of plugins that makes it similar to an ETL tool

- `Input` plugins for ingesting data
- `Filter` plugins for modifying the data
- `Output` plugins for sending the data elsewhere

## Kibana

Is an open source analytics and visualization platform designed to work with Elasticsearch. You use Kibana to search, view, and interact with data stored in Elasticsearch indices. You can easily perform advanced data analysis and visualize your data in a variety of charts, tables, and maps.

## Beats

Is the platform for single-purpose data shippers. They send data from hundreds or thousands of machines and systems to Logstash or Elasticsearch. It can read data using different Beats like

- `Filebeat` Lightweight shipper for logs ***most commonly used***
- `Metricbeat` Lightweight shipper for metrics ***most commonly used***
- `Packetbeat` Lightweight shipper for network data
- `Winlogbeat` Lightweight shipper for Windows event logs
- `Auditbeat` Lightweight shipper for audit data
- `Heartbeat` Lightweight shipper for uptime monitoring

## X-Pack

Is an Elastic Stack extension that bundles security, alerting, monitoring, reporting, and graph capabilities into one easy-to-install package. Some of its capabilities are

- **Security**: Safeguard your data with a comprehensive security offering that extends to every layer of the stack.
- **Alerting**: Proactively monitor the health of your Elastic Stack.
- **Monitoring**: Visualize the performance of your entire system at a glance.
- **Reporting**: Generate reports that contain data from Elasticsearch aggregations and searches.
- **Graph**: Explore the relationships between the indexed terms in your Elasticsearch data.
- **Machine Learning**: Automatically model the behavior of your Elasticsearch data in real time to identify issues faster, streamline root cause analysis, and reduce false positives.
- **SQL**: Query your Elasticsearch data using SQL.
