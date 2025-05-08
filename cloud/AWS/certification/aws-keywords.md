# AWS keywords

## CloudFront

- **Edge locations**
- **Improve performance**
- **Reduce latency**
- **Static content**

## AWS secrets manager

- **Databases and credentials management**

## RDS

- Uses **replicas**
- **Read replicas**

## [AWS network firewall](https://aws.amazon.com/network-firewall)

- **Traffic flow inspection and filtering**

## QuickSight

- **Business intelligence**
- **Data visualization**

## EC2 instances

- They use **roles** for access management

## Application Load Balancer (ALB)

- **Layer 7**

## Network load balancer (NLB)

- **Layer 4**

## Gateway Load Balancer (GWLB)

- **Inspection purposes**

## Elastic Block Storage (EBS)

- **EBS fast snapshot** (needs to be turned on)

## S3

- **Intelligent tiering**
  - Unpredictable access patterns
  - Minimize costs
- Big objects, not great for small ones
- **Versioning**
- **Object size is <= 5TB**
- **Quick data transfer** with Transfer Acceleration enabled

## ElastiCache

- **Requires code changes**

## DynamoDB

- **NoSQL**, **serverless**, and **fully managed**
- **Milliseconds latency**
- **DAX cluster** for read cache (**microsecond** read latency)
- **Event processing**

## Neptune

- **Graph database**
- Supports streams (no duplicates, strict order)

## Keyspaces (for Apache Cassandra)

- Fully managed
- Open-source, NoSQL distributed database
- Use cases: store IoT devices info, time-series data, etc...

## Quantum Ledger Database (QLDB)

- **Discontinued** with end of support on 07/31/2025
- **Ledger of financial transactions**
- You can **review history** and it is inmutable

## Timestream

- **Time series database**
- Store and analyze trillions of events per day
- Well suited for IoT data

## Athena

- **Analyze data in S3** using **serverless SQL**

## Elastic Map Reduce

- **Data processing**
- **Machine learning**
- **Web indexing**
- **Big data**

## Rekognition

- Face detection, labeling, and recognition

## Transcribe

- Audio to text
- **Personally Identifiable Information (PII)** redaction

## Polly

- Text to speech
- Pronunciation lexicons
- Speech Synthesis Markup Language (SSML)

## Translate

- Language translation

## Lex

- Conversational interfaces
- **Chatbots**

## Connect

- **Contact center**

## Comprehend

- Natural language processing
- **Medical**
- Can redact PII in medical records

## SageMaker

- Machine learning
- Data science

## Kendra

- **ML search engine**

## Personalize

- Real-time **personalized recommendations**

## Textract

- Text and data from documents

## CloudWatch

- **Log insights**
- **Container/Lambda/contributor/application insights**

## Key Management Service (KMS)

- **Encryption** for an AWS service

## Secrets Manager

- **Secrets** for **RDS** or **Aurora**

## Elastic File Storage (EFS)

- **Shared file storage** among **EC2 instances**
