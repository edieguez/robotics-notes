# [EC2 (Elastic Cloud Compute)](https://aws.amazon.com/ec2/)

It goes under the category *Infrastructure as a Service*. Its main capabilities are

- Rent virtual machines (EC2)
- Storing data on virtual drives (EBS)
- Distributing load across machines (ELB)
- Scaling the services using an auto-scaling group (ASG)
- Web service that provides resizable compute capacity in the cloud
- Designed to make web-scale cloud computing easier for developers
- **Resources cannot be changed without downtime**

## [Instance types](https://aws.amazon.com/ec2/instance-types)

> For a general guide about the resources each instante has, [check this page](https://instances.vantage.sh)

1. General purpose
2. Compute optimized
3. Memory optimized
4. Accelerated computing
5. Storage optimized
6. Instance features
7. Measuring instance performance

## [Naming conventions](https://docs.aws.amazon.com/ec2/latest/instancetypes/instance-type-names.html)

- `t2.micro` - `t` stands for `burstable performance`, `2` stands for the generation, and `micro` stands for the size
- `m5.large` - `m` stands for `general purpose`, `5` stands for the generation, and `large` stands for the size
- `c5.xlarge` - `c` stands for `compute optimized`, `5` stands for the generation, and `xlarge` stands for the size
- `p3.2xlarge` - `p` stands for `accelerated computing`, `3` stands for the generation, and `2xlarge` stands for the size
- `i3en.24xlarge` - `i` stands for `storage optimized`, `3` stands for the generation, and `24xlarge` stands for the size
- `z1d.large` - `z` stands for `instance features`, `1` stands for the generation, and `large` stands for the size
- `r5a.4xlarge` - `r` stands for `memory optimized`, `5a` stands for the generation, and `4xlarge` stands for the size
- `u-6tb1.metal` - `u` stands for `bare metal`, `6tb1` stands for the generation, and `metal` stands for the size
- `mac1.metal` - `mac` stands for `mac instance`, `1` stands for the generation, and `metal` stands for the size

## Sizing and configuration options

- Operating system
  - Linux
  - Windows
  - Mac OS
- How much compute power and cores (CPU)
- How much random-access memory (RAM)
- How much storage space
  - Network-attached (EBS or EFS)
  - Hardware (EC2 instance store)
- Network card
  - Speed of the card
  - Public IP address
- Firewall rules
  - Configured through a `security group`
- Bootstrap script
  - Runs at first launch

## Root device storage

- `Instance storage` is temporary storage that is available only during the lifetime of the instance. It is not persistent. It is physically attached to the host computer. It is ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers.
- `Elastic block store EBS` is persistent storage that can be attached to an instance. It is independent of the lifetime of the instance. It is ideal for data that requires long-term persistence, such as your operating system and applications, or for data that persists independently of the instance, such as data bases and log files.

## See also

- [Amazon Machine Images (AMIs)](../ami.md)
