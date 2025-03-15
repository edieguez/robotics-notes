# Relation Database Service (RDS)

Managed database for DB that use SQL as query language

- Postgres
- MySQL
- MariaDB
- Oracle
- Microsoft SQL server
- IBM DBZ
- Aurora (Amazon proprietary database)

## RDS auto scaling

- Can increase storage dynamically
- You can set your `maximum storage threshold`
- Automatically modify storage if
  - Free space is less than 10%
  - Low storage last at least 5 minutes
  - 6 hours have passed since last modification

## Read replicas vs multi AZ

- Up to 15 replicas
- Within AZ, cross AZ or cross region
- Replication is **async**. **This means reads are eventually consistent**
- Replicas can be promoted to their own database
- Applications must update their connection string to leverage to the read replica
- There is a cost if your data goes from one AZ to another
  - You don't pay that fee if your replicas are in the same region

## RDS multi AZ (disaster recovery)

- **Replication is made in a sync fashion**
- **One DNS name. That means automatic failover to `standby`**
- **Increases availability**
- Failover is case of
  - Loss of AZ
  - Loss of network
  - Instance or storage failure
  - Read replicas can also be multi AZ

## From single AZ to multi AZ

- Zero downtime operation. No need to stop the DB
- Just click on `modify` to enable it

## Process for replication

1. Snapshot is taken
2. A new database is restored in the new AZ using thar snapshot
3. `Sync` between databases is enabled

## RDS backups

- Automated backups
  - Daily full backup during backup window
  - Logs backed up every 5 minutes
  - Can be restored from oldest backup to 5 minutes ago
  - 1 to 35 days retention. Set to zero to disable backups
- Manual backups
  - Triggered by user
  - Retention is as long as you want

## RDS proxy

- Fully managed by AWS
- Allows apps to pool connections
- Reduces the stress in database resources
- Serverless autoscaling and highly available (multi AZ)
- Reduces failover time by 66%
- Supports RDS (MySQL, Postgres, MariaDB, MS server) and Aurora (MySQL and Postgres)
- Enforce IAM authentication and store credentials in AWS Secrets Manager
- **Never accesible from outside. Needs to be used with VPC**

## RDS and [Aurora](aurora.md) security

1. `At rest encryption`
   - Uses AWS KMS - must be defined at launch
     - Master and replicas are encrypted
     - If master is not encrypted, replicas aren't as well
   - Process to encrypt an unencrypted database
    1. Generate snapshot
    2. Restore it as encrypted
2. `In-flight encryption` TLS ready by default. Use the AWS TLS root certificates client-side
3. `IAM authentication` uses IAM roles to connect to your database (user/pass not recommended)
4. `Security groups` control network access to your database
5. **No SSH unless you are using RDS custom**
6. Audit logs can be enabled and sent to CloudWatch for longer retention

> **To save costs in a predictable workload**
>> If you stop RDS you need to pay for storage. You can snapshot and restore instead

## See also

- [RDS custom](rds-custom.md)
- [Amazon Aurora](aurora.md)
