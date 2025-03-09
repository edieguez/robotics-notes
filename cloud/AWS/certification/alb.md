# Application Load Balancer (ALB)

- Can redirect traffic based on
  1. Hostname
  2. Path
  3. Query string
  4. Headers

## HTTP headers

The following headers are added by the ALB. Can be used to depermine the original client IP address, port and protocol. **Using these names in your own headers is not recommended**

- `X-Forwarded-For` - The IP address of the client
- `X-Forwarded-Port` - The port of the client
- `X-Forwarded-Proto` - The protocol (HTTP/HTTPS)
