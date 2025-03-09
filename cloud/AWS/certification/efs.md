# Elastic File System (EFS)

- Managed NFS (Network File System)
- Can be used with any EC2
- Highly available, scalable, expensive (3x gp2)
- Available on any AZ at the same time
- File system scales automatically
- Performance mode. Need to be activated at creation time

## Throughput modes

- `Bursting (default)` scales as you need, up to 100 MiB/s
- `Provisioned` you can choose the throughput you need (up to 100 MiB/s)
- `Elastic` can burst beyond 100 MiB/s

## Storage tiers

- `Standard` for frequently accessed files
- `Infrequent access` cost more to retrieve files but lower price to store
- `Archive` lowest cost, takes minutes to access. **It is about 50% cheaper**

## Availability and durability

- `standard` storage class is replicated across multiple AZ
- `One Zone` storage class is replicated within the same AZ
