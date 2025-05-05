# Key Management Service (KMS)

Used to be named as *KMS Customer Master Key*. It was renamed since the name was confusing due similarity with the *AWS Key Management Service* (another AWS service)

**Allows AWS to manage encryption keys for you**. It is fully **integrated with IAM for authorization**.

- Key usage can be audited using `CloudTrail`
- Seamlessly integrated into AWS services
  - EBS
  - S3
  - RDS
  - SSM

As a rule of thumb, **never store your secrets in plaintext, especially in your code**

- **KMS Key Encryption** is also **available thought** API calls using the **AWS SDK and CLI**

## KMS encryption types

### Symmetric (AES-256)

- Single encryption key that is used to encrypt and decrypt data
- You **never get access to the unencrypted key**
  - The **access is provided through the KMS API**

### Asymmetric (RSA and ECC)

- Public (encrypt) and private (decrypt) key pair
- The **public key** can be downloaded
- You can't use the **private key** unencrypted

## KMS key types

- `AWS owned` **(free)** SSE-S3, SSE-SQS, **SSE-DDB (default key)**
- `AWS Managed Key` **free** (aws/service-name. E.g. `aws/s3`)
- `Customer Managed Key (created)` costs **$1.00 per month**
- `Customer Managed Key (imported)` costs **$1.00 per month**
  - You also pay for API calls to KMS (**$0.03 per 10,000 requests**)

## Automated key rotation

- `AWS managed keys` are rotated every **1 years**
- `Customer managed keys` (**must be enabled**) **automatic and on-demand**
- `Imported keys` **only manual rotation using alias**
