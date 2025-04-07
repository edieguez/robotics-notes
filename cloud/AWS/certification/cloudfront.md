# AWS CloudFront

Content Delivery Network (CDN) service that speeds up the distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centers called `edge locations`

- Improves read performance, content is cached at the edge
- Improves users experience
- 216 Point of Presence globally (edge locations)
- `DDoS protection` (because worldwide), integration with `AWS Shield`, `AWS Web Application Firewall`

## CloudFront Origins

### S3 bucket

- For distributing files and caching them at the edge
- Enhanced security with `Origin Access Control (OAC)`
  - OAC is replacing `Origin Access Identity (OAI)`
- CloudFront can be used as an ingress (to upload files to S3)

### Custom Origin (HTTP)

- Application Load Balancer
- EC2 instance
- S3 website (must first enable the bucket as a static S3 website)
- Any HTTP backend you want

## CloudFront vs S3 Cross Region Replication

### CloudFront

- Global edge network
- Files are cached for a TTL
- **Great for static content that must be available everywhere**

### S3 Cross Region Replication

- Must be setup for each region you want replication to happen
- Files are updated in near real-time
- Real only
- **Great for dynamic content that needs to be available at low-latency in few regions**

## Geo restriction

You can restrict who can access your distribution

- `Allowlist` allow your users to access your content only if they are in one of the countries on a list of approved countries
- `Blocklist` prevent your users from accessing your content if they are in one of the countries on a list of banned countries
- The country is determined using a third-party Geo-IP database

## Pricing classes

1. `Price Class All`: all regions (United States, Europe, Asia, South America, Africa, Australia)
2. `Price Class 200`: most regions but excludes the most expensive regions
3. `Price Class 100`: only the least expensive regions

## Cache invalidation

To do this you need to perform a `CloudFront invalidation`. You can invalidate all files using `*` or do a partial invalidation specifying a path like `/images/*`
