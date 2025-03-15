# Amazon Elastic Cache

Similar to RDS but for in-memory caches. It supports

- Redis
- Memcached

> When using cache, a *cache invalidation* strategy must be implemented to avoid stale data

## Features

- In-memory high performance, low latency
- Helps to reduce database workloads
- Makes applications stateless by moving state to cache
- Fully managed and maintain bu AWS
- **Using it involves huge application changes**

## Redis vs Memcached

### Redis

- Multi AZ with auto failover
- Read replicas and high availability
- Data durability using AOF persistence
- Backup and restore features
- Supports `Sets` and `Sorted sets`

### Memcached

- Multi node for partitioning (sharding)
- No high availability (replication)
  - Unless you are using lambdas
- Non-persistent
- Backup and restore (serverless)
- Multi-threaded architecture

## Cache security

- IAM authentication for Redis
- IAM policies are only used for AWS API level security
- Redis auth
  - You can set user/pass when crating cluster
  - Is an extra level of security on top of security groups
  - Supports SSL in flight encryption
- Memcached
  - Supports SASL-based authentication (advanced)

## Patterns for Elastic Cache

- `Lazy loading` all data is read. Data can become stale in cache
- `Write through` adds/update data on write to DB. No stale data
- `Session store` save session data in cache. It uses TTL features
