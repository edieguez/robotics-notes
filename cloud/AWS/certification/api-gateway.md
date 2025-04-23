# API Gateway

- **API Gateway** is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale

## Integrations

### Lambda

- Integrate with this to have a fully-managed serverless backend

### HTTP

- Expose HTTP endpoints to the internet
- Useful to add
  - Rate limiting
  - Caching
  - User authentication
  - API keys
  - ...

### AWS Services

- Integrate with other AWS services

## Endpoint types

### Edge-optimized

- Requests are routed through the CloudFront Edge locations (improves latency)
- Gateway still lives in only one region

### Regional

- For clients within the same region
- Could manually combine with CloudFront (more control over the caching strategies and the distribution)

### Private

- Only accessible from your VPC
  - Using an interface VPC endpoint (ENI)
- Use a resource policy do define access

## Security

- IAM roles (useful for internal applications)
- Cognito (identity for external users - like mobile users)
- Custom Authorizers (use Lambda to validate tokens)
