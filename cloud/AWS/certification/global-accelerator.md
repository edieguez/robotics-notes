# Global accelerator

A networking service that improves the availability and performance of the applications that you offer to your global users

Can work with the following services

- Elastic IP
- EC2 instances
- ALB (Application Load Balancer)
- NLB (Network Load Balancer)

It also can be **public** or **private**

## Key concepts

- `Unicast IP`  one server holds the IP address
- `Anycast IP` multiple servers hold the same IP address and the client get redirected to the closest one

## Features

### Consistent performance

- Intelligent routing to lowest latency and fast regional failover
- **No issue with client cache since the IP does not change**
- Everything happens in the internal AWS network

### Health checks

- Global accelerator performs health checks on your application endpoints
- If an endpoint fails the health check, the traffic is redirected to healthy endpoints
- Great for disaster recovery

### Security

- Only 2 external IP need to be whitelisted
- DDoS protection thanks to `AWS Shield`

## Global accelerator vs CloudFront

- They both use the AWS global network and its edge locations around the world
- Both services integrate with AWs Shield for DDoS protection

### CloudFront advantages

- Improves performance for both cacheable content (such as images and videos)
- Dynamic content (such as API acceleration and dynamic site delivery)
- content is served at the edge

### Global accelerator advantages

- Improves performance for a wide range of applications over TCP or UDP
- Proxying packets at the edge to application running in one or more AWS regions
- Good fit for non-HTTP use cases such as gaming (UDP) IoT (MQTT) or Voice over IP
- Good for HTTP use cases that require static IP addresses
- Good for HTTP use cases that require deterministic, fast regional failover
