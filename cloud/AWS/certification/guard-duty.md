# Amazon GuardDuty

Intelligent threat detection service that helps protect your AWS accounts and workloads by **continuously monitoring for malicious or unauthorized behavior**. It **uses machine learning** to detect anomalies in your AWS environment

- One click to enable it with **30 days free trial**
- No need to install software
- Input data includes
  - CloudTrail logs
  - CloudTrail management events
  - CloudTrail S3 data events
  - VPC Flow Logs
  - DNS logs

You can setup `EventBridge` to **send notifications to SNS, Lambda**, etc. It also can protect you from **CryptoCurrency attacks** (has a dedicated *finding* for it)
