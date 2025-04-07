# FSx

## FSx for Windows (File Server)

- Fully managed Windows file system share drive
- Supports SMB protocol and Windows NTFS
- Microsoft Active Directory integration, ACL, User quotas
- **Can be mounted on Linux EC2 instances**
- Supports Microsoft Distributed File System (DFS) Namespaces (group files across multiple FS)
- Scale up to 10s of GB/s, millions of IOPS, 100s PB of data
- Can be accessed from your on-premises infrastructure (VPN or Direct Connect)
- **Can be configured to be Multi-AZ (high availability)**
- **Data is backed up daily to S3**

### FSx for Windows storage options

- SSD - Fast performance, low latency
- HDD - Cost-effective, high throughput

## Amazon FSx for Lustre

- Lustre is a type of parallel distributed file system for large-scale computing
- The name Lustre is derived from **Linux** and **cluster**
- Can be used for video processing, financial modeling, electronic design automation
- Scales up to 100s GB/s, millions of IOPS, sub-ms latencies
- **Seamless integration with S3**
  - Can *read S3* as a file system (through FSx)
  - Can write the output of the computations back to S3 (through FSx)
- **Can be accessed from your on-premises infrastructure (VPN or Direct Connect)**

### FSx for Lustre storage options

- SSD - Fast performance, low latency
- HDD - Cost-effective, high throughput

## Fsx File System Deployment Options

### Scratch file system

- Temporary storage
- Data is not replicated (doesn't persist if file server fails)
- High burst (6x faster, 200MBps per TiB)
- Usage: short-term processing, optimize costs

### Persistent File System

- Long-term storage
- Data is replicated within same AZ
- Replace failed files within minutes
- Usage: long-term processing, sensitive data

## Amazon FSx for NetApp ONTAP

- Managed NetApp ONTAP on AWS
- **File system compatible with NFS, SMB, iSCSI protocol**
- Move workloads running on ONTAP or NAS to AWS
- **Storage shrinks or grows automatically**
- Snapshots, replication, low,cost, compression and data de-duplication
- **Point-in-time instantaneous cloning (helpful for testing new workloads)**

### Amazon FSx for NetApp ONTAP operating system compatibility

- Linux
- Windows
- MacOS
- VMware Cloud on AWS
- Amazon Workspaces and AppStream 2.0
- Amazon EC2, ECS and EKS

## Amazon FSx for OpenZFS

- Managed OpenZFS files system on AWS
- File system compatible with NFS (v3, v4, v4.1, v4.2)
- Move workloads running on ZFS wo AWS
- Up to 1,000,000 IOPS with < 0.5 latency
- Snapshots, compression and low-cost
- **Point-in-time instantaneous cloning (helpful for testing new workloads)**

### Amazon FSx for OpenZFS operating system compatibility

- Linux
- Windows
- MacOS
- VMware Cloud on AWS
- Amazon Workspaces and AppStream 2.0
- Amazon EC2, ECS and EKS
