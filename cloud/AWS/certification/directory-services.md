# AWS Directory Services

`Active Directory (AD)` is a service found in any Windows Server with `AD Domain Services`. Is a **objects database** than contains

- User accounts
- Computers
- Printers
- Files shares
- Security groups

Objects are organized in **trees** and a groups of trees is a **forest**

## AWS Managed Microsoft AD

- Create your own AD in AWS, manage users locally and supports MFA
- Establish *trust* connections with your on-premises AD

## AD Connector

- Directory Gateway (proxy) to redirect to on-premise AD, supports MFA
- Users are managed on the on-premises AD

## Simple AD

- AD-compatible directory **managed by AWS**
- **Cannot be joined with on-premise AD**
