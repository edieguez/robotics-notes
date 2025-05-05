# AWS IAM Identity center

*AWS Single Sign-On* sucesor

It gives you **single sign-on** for

- AWS accounts in AWS organizations
- Business cloud applications (e.g. Salesforce, Box, Office 365)
- Custom SAML 2.0 applications
- EC2 Windows instances

It supports the following identity providers

- Built-in identity store in IAM Identity Center
- 3rd party identity providers (e.g. Okta, Azure AD, Google Workspace)

## Fine-grained permissions and assignments

### Multi-account permissions

- Manage access across AWS accounts in your AWS organization
- Permission sets - *a collection or one or more IAM policies* assigned to users and groups to define AWS access

### Application assignments

- SSO access to many SAML 2.0 applications
- Provide required URLs, certificates and metadata

### Attribute-based Access Control (ABAC)

- Fine-grained permissions based on user attributes stored in IAM Identity Center
