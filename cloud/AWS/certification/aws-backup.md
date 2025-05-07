# AWS Backup

AWS Backup is a **fully managed backup service** that makes it easy to centralize and automate the backup of data across AWS services in the cloud as well as on-premises. It also **supports cross-region and cross-account backups**

## Supported services

- Amazon EC2/EBS
- Amazon S3
- Amazon RDS (all DB engines)/Aurora/DynamoDB
- Amazon DocumentDB/Amazon Neptune
- Amazon EFS/Amazon FSx (Lustre and Windows File Server)
- AWS Storage Gateway (volume gateway)

## Features

- Point-in-time Recovery (PITR) for supported services
- On-demand and scheduled backups
- Tag-based backup policies

## Backup plans

A backup plan is a policy that defines how AWS Backup performs backup and restore tasks. It includes

- `Backup frequency` every 12 hours, daily, weekly, cron expression
- `Backup window` start and end time
- `Retention period` how long to keep backups
- `Transition to cold storage` after how long to move backups to cold storage

## Backup Vault Lock

- Enforce a WORM (Write Once, Read Many) model for your backups
- Additional layer of defense to protect your backups against
  - Inadvertent or malicious deletion
  - Updates that shorten or alter the retention period
- Event the root user can't delete or modify the backup vault lock
