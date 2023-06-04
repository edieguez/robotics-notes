# [EC2 (Elastic Cloud Compute)](https://aws.amazon.com/ec2/)

- Web service that provides resizable compute capacity in the cloud
- Designed to make web-scale cloud computing easier for developers
- **Resources cannot be changed without downtime**

See also [AMI](ami.md)

## Categories

1. General purpose
2. Compute, memory and storage optimized
3. Accelerated computing

## Root device storage

- `Instance storage` is temporary storage that is available only during the lifetime of the instance. It is not persistent. It is physically attached to the host computer. It is ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers.
- `Elastic block store EBS` is persistent storage that can be attached to an instance. It is independent of the lifetime of the instance. It is ideal for data that requires long-term persistence, such as your operating system and applications, or for data that persists independently of the instance, such as data bases and log files.
