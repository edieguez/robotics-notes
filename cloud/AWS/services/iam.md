# Identity and Access Management (IAM)

IAM is a **global** service that allows you to manage users, groups, and permissions across all AWS services. IAM is a key component of AWS security and is used to control access to AWS resources.

## IAM security tools

- IAM Credentials Report (account-level)
  - A report that list all your account's users and the status of their various credentials
- IAM Access Analyzer (user-level, renamed to `Last Accessed`)
  - Access advisor shows the service permissions granted to a user and when those services were last accessed
  - You can use this information to revise your policies

## Glossary

- `users` mapped to a physical user, has a password for AWS console
- `groups` a collection of users. **Can have permissions (policies) attached**
- `policies` a document that defines permissions. It is in `JSON` format
- `roles` are attached to EC2 instances or AWS services. **Can have permissions (policies) attached**
- `security` MFA + password policy
- `AWS CLI` manage AWS from the command line
- `AWS SDK` manage AWS using a programming language
- `access keys` used with the CLI and SDK to provide access to AWS
- `audit` `IAM credentials` report and `IAM Access Analyzer`

## See also

- [IAM Policy Simulator](https://policysim.aws.amazon.com/home/index.jsp)
- [IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- [IAM Policy Reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies.html)
