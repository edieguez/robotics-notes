# AWS services index

## Events, messaging and notifications

- `SES` - Simple Email Service
- `Simple Notification Service (SNS)` - Pub/sub messaging service
- `Simple Queue Service (SQS)` - Message queue service
- `Event Bridge` - Serverless event bus. It integrates with third-party services like `Zendesk`, `PagerDuty`, `Datadog`, `Shopify` and `Slack`
- `Step Functions` - Serverless orchestration service. Similar to a state machine

## Identity, security and authentication

- [IAM (Identity and Access Management)](./iam.md)
- `Cognito` - Identity management for your apps. Supports identity providers such as Google, Facebook, and Amazon

## Routing

- [Virtual Private Cloud (VPC)](./vpc.md) - Isolated cloud resources
- [Route 53](./route_53.md) - DNS service
- [Elastic Load Balancing (ELB)](./elb.md) - Load balancer
- `API Gateway` - Create, publish, maintain, monitor, and secure APIs

## Compute

- [Elastic Compute Cloud (EC2)](./ec2.md) - Run virtual servers
- [Lambda](./lambda.md) - Run code without provisioning or managing servers
- [Elastic Container Service (ECS)](./ecs.md) - Run and manage Docker containers
- [Elastic Kubernetes Service (EKS)](./eks.md) - Run Kubernetes on AWS

## Storage

- [`S3` - Simple Storage Service](./s3.md)
- [`S3` Glacier - Long-term storage](./s3-glacier.md)
- [`EBS` - Elastic Block Storage](./ebs.md)
- [`EFS` - Elastic File System](./efs.md)
- [`Amazon FSx for Windows File server` - Windows file server](./fsx.md)
- [`AWS snowball` - Physical data transport](./snowball.md)
- [`AWS snowmobile` - Physical data transport](./snowmobile.md)

### Data warehousing or data lakes

- `RedShift` - Data warehousing
- `Quicksight` - Business intelligence. **Dashboards and visualizations**

## Analytical processing

- `Athena` - Query data in S3 using SQL
- `Elastic MapReduce (EMR)` - Big data processing

## Caching

- `Elastic Cache` - In-memory data store
- [CloudFront](./cloudfront.md) - Content delivery network

## Databases

- `Amazon Aurora` - MySQL and PostgreSQL-compatible relational database built for the cloud
- `Relational Database Service (RDS)` - Managed relational database service. Supports MySQL, PostgreSQL, MariaDB, Oracle, and SQL Server
- `DynamoDB` - Managed NoSQL database
- `DocumentDB` - Managed document database. Compatible with MongoDB
- `OpenSearch Service` - Managed Elasticsearch service
- `AppSync` - Managed GraphQL service

## Package infrastructure

- [Elastic Beanstalk](./beanstalk.md) - Platform as a service
- `CloudFormation` - Infrastructure as code. It can work with `Cloud Development Kit (CDK)` to define cloud resources in code
- `App Runner` - Fully managed container service. It uses `ECS` and `Fargate` under the hood
- `Lightsail` - Virtual private server and web hosting
- `Amplify` - Deploy resources using a CLI or the Amplify Console
- `Serverless Application Model (SAM)` - Framework for building serverless applications

## Deployment orchestration

> All of these services work together to provide a continuous integration and continuous deployment (CI/CD) pipeline

- `Code commit` - Git repository hosting
- `Code build` - Build service
- `Code deploy` - Deployment service
- `Code pipeline` - Continuous integration and continuous deployment service

## Monitoring

- `CloudWatch` - Monitor resources and applications
- `CloudTrail` - Log, continuously monitor, and retain account activity related to actions across your AWS infrastructure
