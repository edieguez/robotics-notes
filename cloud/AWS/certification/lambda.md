# AWS Lambda

- Free tier
  - 1M requests per month
  - 400,000 GB-seconds of compute time per month
- Virtual functions in the cloud. Only code, no servers to manage
- **Run on-demand. Pay for what you use**
- Event-driven: can be invoked by other AWS services
- **Scaling is automated**
- Monitoring through CloudWatch

## Limits (per region)

### Execution

- From 128MB up to 10GB RAM per function (1MB increments)
- Execution time up to 15 minutes
- 4KB for environment variables
- From 512MB up to 10GB for temp storage (in `/tmp`)
- 1,000 concurrent executions (can be increased through a support ticket)

### Deployment

- Size
  - Compressed package: 50MB
  - Uncompressed package: 250MB (code + dependencies)

## SnapStart

- Supports `Java`, `Python` and `.NET`
- The VM in pre initialized so the function can start faster

## RDS proxy

If your Lambda functions access your RDS database, they may overload it. To avoid this, you can use RDS proxy

- Improves scalability by pooling and sharing DB connections
- Improve availability by **reducing by 66% the failover time and preserving connections**
- **RDS proxy is never publicly available**
  - Therefore your Lambda must be deploy in your VPC

### RDS and Aurora

- You can invoke lambda functions within your database
  - This can be used to process **data events**
- Supports
  - RDS for PostgreSQL
  - Aurora MySQL
- Outbound traffic to your lambda must be allowed
  - Public
  - NAT
  - GW
  - VPC endpoint

## Event notifications

Can be send to `SNS` and `EventBridge`. **You don't get information about the data itself**, only about the event

- DB instance
- DB snapshot
- DB parameter group
- DB security group
- RDS proxy
- Custom engine version

## See also

- [Aurora](./aurora.md)
