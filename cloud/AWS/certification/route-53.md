# Amazon Route 53

Highly available, scalable, fully managed and [Authoritative](https://www.cloudns.net/blog/authoritative-dns-server/#:~:text=The%20authoritative%20DNS%20server%20is,information%20cached%20in%20its%20memory.) DNS

> The authoritative DNS server is the final holder of the IP of the domain you are looking for. When you write a domain name in your browser, a DNS query is sent to your internet service provider (ISP). The ISP has a recursive server, which might have the needed information cached in its memory.

- The customer (you) can update the DNS records
- Is also a name registrar
- Can check the health of your resources
- Is the only AWS with 100% SLA
- The *53* is a reference to the DNS port number

## Records structure

- `Domain/subdomain name`
- `Record type` e.g. A or AAAA
- `Value` e.g. 192.168.1.10
- `Routing policy` how Route 53 responds to queries
- `TTL` Time To Live for cache invalidation

## Supported DNS record types

- Must know
  1. A
  2. AAAA
  3. CNAME
  4. NS
- Advanced
  1. CAA
  2. DS
  3. MX
  4. NAPTR
  5. SOA
  6. TXT
  7. SPF
  8. SRV

### Record types

- `A` hostname to IPv4
- `AAAA` hostname to IPv6
- `CNAME` hostname to hostname
  - Target is a domain name with an A or AAAA record
  - Can't create a CNAME for the top node of a DNS namespace (zone apex)
  - Example: you cannot create a CNAME for `example.com` buy you can create a CNAME for `www.example.com`

## Hosted zones

Is a container for records that define how to route to a domain and its subdomains

- `Public hosted zones` records to route traffic on the internet (public domain names)
- `Private hosted zones` records to route traffic within one or multiple VPC (private domain names)

## CNAME vs alias

- Points to a hostname
  - **Only for non-root domain
- Alias
  - Points to an AWS resource
  - It works for root and non-root domains
  - **It only works with Route 53 since it uses an ARN**
    - In other words, it is not part of the DNS protocol
  - Alias record is type A/AAAA for AWS resources (IPv4 and IPv6)
  - You can set TTL. It is handled by Route 53

## Posible targets for aliasing

- Elastic Load Balancers
- CloudFront distributions
- API gateway
- Elastic Beanstalk environments
- S3 websites (there is an option to enable S3 as a website)
- VPC interface endpoints
- Global Accelerator
- **Router 53 record in the same AZ**

> **You cannot set an alias for an EC2 DNS name**

## Routing policies

Defines how Route 53 responds to DNS queries

1. `Simple` usually singe vale. If multiple values are return, a random value is chosen by the client
2. `weighted`
   - Controls the percentage or request that go to each resource
   - DNS records must have the same name and type
   - Can be associated with health checks
   - Weight - stops sending requests to the resource
   - If all records hace weight of 0, all records will be equally forwarded
3. `Failover` It has a primary record. If that fails, it responds with a failover record
4. `Latency based` Redirect to the resource with less latency
5. `Geolocation` Based on location. If no match, default record is returned
6. `Multi-value answer` Up to 8 values returned. Does not replace ELB
7. `Geoproximity` (with Route 53 traffic flow feature). Shifts the traffic using a bias to favor certain locations
8. `IP based routing` Requires CIDR (Classless Inter Domain Routing)

### Health checks

- **Can be performed in public resources only**
- Amazon has about 15 global health checkers
  - Healthy/unhealthy - 3 (default)
  - 30 seconds interval. Down to 10 seconds with higher cost
  - HTTP, HTTPS and TCP
  - If less than 18% report healthy, Route 53 reports healthy. Otherwise unhealthy
- Health checks pass when `2xx` or `3xx` status code is returned
- Can check response in the first `5,120` bytes of the response
- Calculated health checks: multiple health checks into one
  - Can use `AND`, `OR` and `NOT`
  - Up to 256 child health checks
- Private resources need to be monitored using CloudWatch metrics
  1. Set an alarm
  2. Create health check using that alarm
