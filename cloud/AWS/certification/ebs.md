# Elastic Block Store (EBS)

- Block storage service that you can use with EC2 instances
  - **One EBS volume can be attached to one EC2 instance at a time**
- Uses network to communicate. Some latency is expected
- Supports snapshots. Detachment is recommended but not required
- Locked to specific availability zone
  - You can't move an EBS but you can move a snapshot
- You need to define capacity in IOPS from the beginning
- Can be deleted on termination

## EBS volume types

### General Purpose SSD (gp2)

- Cost effective with low latency

### Provisioned IOPS SSD (io1)

- For apps that need more than 16,000 IOPS
- Great for database workloads
- Business apps with sustained IOPS performance
- Supports EBS multi-attach

### Throughput Optimized HDD (st1)

- **Cannot be a boot volume**
- **125 GiB to 16 TiB**
- Throughput optimized

### Cold HDD (sc1)

- For less frequently accessed data
- Lower cost

## EBS snapshot options

### EBS snapshot archive

- 75% of the cost of the original volume
- Takes from 24 to 48 hours to 72 hours to restore

### Recicle bin grom EBS snapshots

- Setup rules for recovery in case of accidental deletion
- Retention from 1 day to 1 year

### Fast snapshot restore (FSR)

- Restore a snapshot in seconds
- It is more expensive buy way faster

## EBS multi-attach

- The EBS need to be in the same AZ as the instances
- Each instance can read and write to the EBS
- **Up to 16 instances at time**
