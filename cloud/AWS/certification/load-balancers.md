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

## Application Load Balancer (ALB)

Can redirect traffic based on

- Query params
- Fixed hostname

It adds the following headers to the request

- `X-Forwarded-For` - The IP address of the client
- `X-Forwarded-Proto` - The protocol used by the client
- `X-Forwarded-Port` - The port used by the client

## Network Load Balancer (NLB)

- Works in layer 4 (OSI model)
  - Allows TCP and UDP traffic
- Has one public IP per AZ
  - Supports Elastic IP addresses
  - Helpful when whitelisting
- Ideal if extreme performance is needed
- Uses target groups

## Gateway Load Balancer (GWLB)

- Deploy, scale and manage a fleet of 3rd party network virtual appliances in AWS
- Operates at layer 3 (network layer - IP packets)
- Has two main functions
  1. Transparent Network Gateway
  2. Load balancer
- Uses GENEVE protocol on port 6081

## Sticky sessions

The same client always get redirected to the same instance behind a load balancer

- It works using a cookie
- Can be used with
  1. classic Lad Balancer
  2. Application Load Balancer
  3. Network Load Balancer
- Enabled for ALB (free)
- Disabled by default for NLB and GWLB
  - If you activate it, Amazon will start charging you

## SSL certificates

> **SSL** Secure Sockets Layer
> **TLS** Transport Layer Security. Most used nowadays. **People still refer to it as SSL**

## Connection draining

- Stops sending new requests to an instance that is deregistering
- It has different names depending the service
  1. `Connection draining` - Classic Load Balancer
  2. `Deregistration delay` - Application Load Balancer and Network Load Balancer

## References

- [What is GENEVE?](https://www.redhat.com/en/blog/what-geneve)
- [RFC 8926 Geneve: Generic Network Virtualization Encapsulation](https://www.rfc-editor.org/rfc/rfc8926)
