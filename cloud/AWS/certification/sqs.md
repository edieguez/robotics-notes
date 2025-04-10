# Amazon SQS

It is one of the oldest AWS services (over 10 years old). Is fully managed and **it is used to decouple applications**

## Attributes

- Unlimited throughput
- Unlimited number of messages in queue
- Messages are short-lived
  - At least 4 days retention
  - Maximum 14 days
- Low latency (less than 10 milliseconds on publish and receive)
- Limitation of 256kb per message sent

## Caveats

- Can have duplicate messages
- Can have out of order messages

## Message life cycle

1. Message produced to SQS using the SDK (SendMessage API)
2. The message is persisted in SQS until a consumer reads it (consume) or the retention period expires

## Consuming messages

- Messages are consumed by polling the SQS queue
- Consumers can be
  - EC2 instances
  - Lambda functions
  - On-premises applications
- Consumers receive and precess messages in parallel
- At least once delivery
- Best-effort message ordering
- Consumers delete messages after processing them
- We can scale consumers horizontally to improve throughput

## Security

### Encryption

- In-flight encryption using HTTPS API
- At-rest encryption using KMS keys
- Client-side encryption. You will need to perform the encryption/decryption in your application

### Access controls

- IAM policies to regulate access to the SQS API

### SQS access policies (similar to S3 bucket policies)

- Useful for cress-account access to SQS queues
- Useful for allowing other services (SNS, S3, etc) to write to an SQS queue

## Message visibility timeout

- After a message is polled by a consumer it becomes *invisible* to other consumers
- The message is not deleted, but it is not visible
- This has a *30 seconds cool down*
  - That means the message has 30 seconds to be processed
- After that time, the message becomes visible again if it hasn't been deleted by the previous consumer
- **This can potentially lead to the same message being processed twice**
  - If you need more time to process the message, you can call `ChangeMessageVisibility` API to get more time

## Long pooling

When a client connect and there are no messages it can wait for new messages to arrive. This is called `long pooling`. It is more cost-effective and therefore, preferred than `short pooling`. This behavior can be enabled at API by using the `WaitTimeSeconds` parameter

## Amazon SQS: FIFO queue

- Fist In First Out queue
  - This means order is strictly preserved
- Lower throughput than standard queues
- Messages are processed in order by the consumer
- Messages are sent exactly once
- No duplicates
- Ordering happens at group level (not queue level)
  - That means `Message Group ID` is mandatory

## SQS with Auto Scaling Group (ASG)

If your queue gets a lot of messages, you can scale the consumers using an ASG. This way you can scale the number of EC2 instances processing the messages. This is done be using a `CloudWatch alarm` on the `ApproximateNumberOfMessagesVisible` metric. **This will force the ASG to add more EC2 instances**
