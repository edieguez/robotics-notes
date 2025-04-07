# S3 Batch operations

- Perform bulk operations on existing S3 objects with a single request
  - Modify object metadata and properties
  - Copy objects to another bucket
  - **Encrypt un-encrypted objects**
  - Modify ACLs, tags, etc
  - Restore objects from S3 Glacier
  - Invoke Lambda function to perform custom action on each object
- A job is a list oj objects, the action to perform, and optional parameters

## Why to use S3 Batch Operations?

- Manages retries
- Tracks progress
- Sends completion notifications
- Generate reports
