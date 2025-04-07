# S3 access points

Is a feature of **S3** that simplifies managing data access at scale for shared data sets in **S3**. It allows you to create access points with names and permissions that apply to any request made through the access point

You can think about them as aliases for buckets, they are network endpoints that you can use to access **S3** buckets. They simplify managing data access at scale for shared data sets in **S3**. Access points are unique hostnames that customers create to enforce distinct permissions and network controls for any request made through the access point

- Access Points simplify security management for S3 buckets
- Each Access Point has
  - Its own DNS name (Internet or VPC endpoint)
  - Access point policy (similar to bucket policy)
