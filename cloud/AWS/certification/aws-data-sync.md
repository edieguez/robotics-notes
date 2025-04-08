# AWS DataSync service

**Data transfer service** that simplifies, automates, and accelerates moving data between on-premises storage and AWS storage services

- Move large amount of data to and from
  - On-premises/other cloud to AWS (NFS, SMB, HDFS, S3, API...) - **needs agent**
  - AWS to AWS (different storage services) - **doesn't need agent**
- Can synchronize to
  - Amazon S3 (any storage classes - including Glacier)
  - Amazon EFS
  - Amazon FSx (Windows, Lustre, NetApp, OpenZFS...)
- Replication tasks can be scheduled hourly, daily weekly
- **File permissions and metadata are preserved (NFS POSIX, SMB...)**
- One agent task can use 10 Gbps. A bandwidth limit can be set
