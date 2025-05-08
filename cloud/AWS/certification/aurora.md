# [Amazon Aurora](https://aws.amazon.com/rds/aurora)

- Proprietary tech from Amazon
- Drivers for Postgres and MySQL work with Aurora
- It is *cloud optimized*
  - 5 times better performance than MySQL
  - 3 times better performance than Postgres
- Storage grows from 10GB up to 128TB
- Up to 15 replicas
  - Faster than MySQL (< 10 minutes replica lag)
  - Failover is instantaneous
- 20% more expensive than RDS but it is also more effective

## High availability and read scaling

- 6 copies of your data across 3 availability zones
  - 4 copies out of 6 needed for writes
  - 3 copies out of 6 needed for reads
  - Self-healing using peer-to-peer replication
  - Storage striped across more than 100 volumes

## Features

- Automatic failover
- Backup and recovery
- Isolation and recovery
- Industry compliance
- Push button scaling
- Automatic patching with zero downtime
- Advanced monitoring
- Routine maintenance
- `Backtracking` restore data to any point of th time without using backups

## Aurora serverless

- Instantiation and scaling based in actual usage
- Good for infrequent, intermittent or unpredictable workloads
- No capacity planning needed
- **Pay per second. Can be more cost effective**

## Aurora backups

- Cannot be disabled
- Point in time recovery within a time frame
- Manual backups
  - Triggered by user
  - Retention is as long as you want

## Aurora database cloning

- New Aurora database from an existing one
- Faster than snapshot and restore
- **Uses copy-on-write protocol**
- **Fast and cost effective**
- Use case: create staging env with prod data

## See also

- [RDS](rds.md)
- [RDS custom](rds-custom.md)
