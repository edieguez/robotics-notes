# AWS storage gateway

Is a bridge between on-premises data and cloud data

- Configured S3 buckets are accessible using the NFS and SMB protocols
- **Most recently used data is cached in the file gateway**
- Supports S3 Standard, S3 Standard IA, S3 One Zone A, S3 Intelligent Tiering
- **Transition to S3 Glacier using a Lifecycle Policy**
- Bucket access using IAM roles for each File Gateway
- SMB Protocol has integration with Active directory (AD) for user authentication

## Amazon FSx File Gateway (discontinued)

- Native access to Amazon FSx for Windows File Server
- **Local cache for frequently accessed data**
- Windows native compatibility (SMB, NTFS, Active Directory)
- Useful for group file shares and home directories

## Volume gateway

- Block storage using iSCSI protocol backed by S3
- Backed by EBS snapshots which can help restore on-premises volumes
- `Cached volumes` low latency access to most recent data
- `Stored volumes` entire dataset is on premise, scheduled backups to S3

## Tape gateway

- Some companies have backup processes using physical tapes (D:)
  - It is the same process but in the cloud
- Virtual Tape Library (VTL) backed by Amazon S3 and Glacier
- Back up data using existing tape-based processes (and iSCSI interface)
- Works with leading backup software vendors

## Storage gateway - Hardware appliance

- Is a literal server which means you need in-premises virtualization
- Can be bought on `amazon.com`
- Works with File Gateway, Volume Gateway, Tape Gateway
- Has the required CPU, memory, network, and storage resources
- Helpful for daily NFS backups in small data centers
