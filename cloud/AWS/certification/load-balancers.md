# Load balancers

- `Classic Load Balancer` (CLB) - Layer 4 (TCP/SSL) & Layer 7 (HTTP/HTTPS) - **deprecated**
- `Application Load Balancer` (ALB) - Layer 7 (HTTP/HTTPS)
- `Network Load Balancer` (NLB) - Layer 4 (TCP/SSL)
- `Gateway Load Balancer` (GWLB) - Layer 3 (IP)
  - Can be internal (private) and external (public)
  - Good for microservices and container based applications
  - Has port-mapping capabilities to redirect to ECS

## Target groups

Are used to route requests to one or more registered targets. When you create a target group, you specify a target type, protocol, and port.

They can be used with the following components

- EC2 instances
- ECS tasks
- Lambda functions
- IP addresses (must be private)
