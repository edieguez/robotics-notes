# S3 Lifecycle Rules

- Rules can be created for a certain prefix (example: `s3://mybucket/logs/*`)
- Rules can be created for certain objects Tags (example: `Department: Finance`)

## Transition actions

Configure objects to transition to another storage class

- Move objects to Standard IA class 60 days after creation
- Move to Glacier for archiving after 6 months

## Expiration actions

Configure objects to expire (delete) after some time

- Access log files can be set to delete after a 365 days
- Can be used to delete old versions of files (if versioning is enabled)
- Can be used to delete incomplete Multi-Part uploads
