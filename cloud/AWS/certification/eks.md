# Amazon Elastic Kubernetes Service (EKS)

It is a way to launch and manage Kubernetes clusters on AWS

- It is an alternative to [ECS](ecs.md), similar goal but different API
- Unlike `ECS`, `Kubernetes` is open source
- Supports `EC2` if your want to deploy worker nodes of `Fargate` to deploy serverless containers
- **Kubernetes is cloud-agnostic** that means it can be used on any cloud
- When you see the term `parts`, Kubernetes may be involved

## Node types

### Managed node groups

- Creates and manages nodes (EC2 instances) for you
- Nodes are part of an ASG managed by EKS
- Supports On-Demand or Spot Instances

### Sef-managed nodes

- Nodes created by your an registered to the EKS cluster and managed bu an ASG
- You can use prebuilt AMI - Amazon EKS optimized AMI
- Supports On-Demand or Sport instances

### AWS Fargate

- No maintenance required; no nodes managed

## Data volumes

- Need to specify **StorageClass** manifest on your EKS cluster
- Leverages a **Container Storage Interface (CSI)** compliant driver

### Supported storage services

1. Amazon EBS
2. Amazon EFS (the only one that works with `Fargate`)
3. Amazon FSx for Lustre
4. Amazon FSx for NetApp ONTAP
