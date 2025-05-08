# [Elastic File System (EFS)](https://aws.amazon.com/efs)

- Managed NFS (Network File System)
- Can be used with any EC2
- Highly available, scalable, expensive (3x gp2)
- Available on any AZ at the same time
- File system scales automatically
- Performance mode. Needs to be activated at creation time

## Throughput modes

- `Bursting (default)` scales as you need, up to 100 MiB/s
- `Provisioned` you can choose the throughput you need (up to 100 MiB/s)
- `Elastic` can burst beyond 100 MiB/s

## Performance modes

- `General purpose` latency-sensitive use cases
  - Web serving
  - Content management
  - Home directories
- `Max I/O` high-performance use cases
  - Big data
  - Media processing
  - Genomic analysis

## Storage tiers

- `Standard` for frequently accessed files
- `Infrequent access` cost more to retrieve files but lower price to store **(up to 92% compared to *standard*)**
- `Archive` lowest cost, takes minutes to access. **It is about 50% cheaper**

## Availability and durability

- `standard` storage class is replicated across multiple AZ
- `One Zone` storage class is replicated within the same AZ
