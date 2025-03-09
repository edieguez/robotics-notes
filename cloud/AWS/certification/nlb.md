# Network Load Balancer (NLB)

- Works in layer 4 (TCP/SSL)
  - **Allows TCP and UDP**
- **As one public OP per AZ**
  - Supports Elastic IP
  - Helpful when whitelisting
- Uses `target groups` to route requests to one or more registered targets
