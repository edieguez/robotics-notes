# Amazon Inspector

**Automated security assessments** to help improve the security and compliance of applications deployed on AWS

- Reporting and integration with `AWS security hub`
- Send findings to `Amazon EventBridge`

## EC2 instances

- Leverages the **AWS System Manager(SSM) agent**
- Analyze against unintended network accessibility, remote root login, and software vulnerabilities
- Analyze the running OS against known vulnerabilities

## Container Images push to Amazon ECR

Scans the images for **CVEs** and **security best practices**. It can be integrated with **CodeBuild** to scan images before pushing them to ECR

## Lambda functions

- Identifies software vulnerabilities in function code and package dependencies
- Assessment of functions as they are deployed
