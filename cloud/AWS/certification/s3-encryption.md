# S3 encryption

You have four methods to encrypt your data in a S3 bucket

> `SSE` Server Side Encryption

## `Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)`

- Enabled by default for new buckets and objects
- Encrypts S3 objects using keys handled, managed and owned by AWS
- Object is encrypted server-side
- Encryption type is `AES-256`
- Must set header `x-amz-server-side-encryption: AES256` to encrypt object

## `Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)`

- Encryption using keys handled, managed and owned by AWS Key Management Service
- KMS Advantages:
  - User control over encryption keys
  - Audit trail of when keys were used
  - Automatic rotation of keys
  - Disable/Enable key usage
  - Integrated with AWS CloudTrail to provide logs of when keys are used
  - Can be used to enforce encryption of objects
- Object is encrypted server-side
- Must set header `x-amz-server-side-encryption: aws:kms` to encrypt object

### SSE-KMS limitation

If you use SSE-KMS your may be impacted by the KMS limits

- On upload, it calls the **GenerateDataKey** KMS API
- On download, it calls the **Decrypt** KMS API
- It has a quota per second: 5,500, 10,000, 30,000 request per second based on region
- **You can request a quota increase using the `Service Quotas console`**

## `Double Server Side Encryption with AWS KMS-managed Keys (DSSE-KMS)`

- Same as SSE-KMS but with an additional envelope of encryption

## `Server-Side Encryption with Customer-Provided Keys (SSE-C)`

- When you want to manage your own encryption keys
- Amazon S3 does not store the encryption key you provide
- **Since you are sending your key over the internet, HTTPS must be used**
- Encryption key must be provided in the header of every HTTP request made

## `Client-Side Encryption`

- Use client libraries such a `Amazon S3 Client-Side Encryption Library`
- Clients must encrypt data themselves before sending to Amazon S3
- Clients must decrypt data themselves when retrieving from Amazon S3
- Customer is responsible for managing the files encryption cycle

## Encryption in transit

- Encryption in flight is also called SSL/TLS
- S3 exposes two endpoints
  1. **HTTP endpoint** - not encrypted
  2. **HTTPS endpoint** - encryption in flight
- HTTPS is recommended
- HTTPS is mandatory for `SSE-C`

## Force encryption in transit

To achieve this you can use a `S3 policy`

```json
{
    "Version": "2012-10-17",
    "Statement": [
        "Effect": "Deny",
        "Principal": "*",
        "Action": "s3:GetObject",
        "Resource": "arn:aws:s3:::my_secure_bucket/*",
        "Condition": {
            "Bool": {
                "aws:SecureTransport": "false"
            }
        }
    ]
}
```
