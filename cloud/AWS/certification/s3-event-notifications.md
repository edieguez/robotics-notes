# S3 event notifications

Can generate events that can be consumed by the following services

- Simple Notification Service (SNS)
- Simple Queue Service (SQS)
- Lambda functions

Event notifications can be triggered by the following events. This is not an exhaustive list

- `s3:ObjectCreated:*`
- `s3:ObjectRemoved:*`
- `s3:ObjectRestore:Completed`
- `s3:ReducedRedundancyLostObject`
- `s3:Replication:OperationFailedReplication`

> Notifications typically deliver within seconds but can sometimes take a minute or longer

This feature can be also integrated with `Amazon EvenBridge` to trigger events in other AWS services
