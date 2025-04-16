# Amazon Elastic Container Service (ECS)

## Overview

Amazon Elastic Container Service (ECS) is a container management service that makes it easy to run, stop, and manage Docker containers on a cluster. Amazon ECS lets you launch and stop container-based applications with simple API calls, allows you to get the state of your cluster from a centralized service, and gives you access to many familiar Amazon EC2 features.

## Launch types

### EC2 launch type

In the EC2 launch type, you run your containerized applications on a cluster of Amazon EC2 instances that you manage.

- You must provision and maintain the infrastructure (that is, the EC2 instances)
- Each instance must run the `ECS Agent` to register in the `ECS Cluster`

### Fargate launch type

In the Fargate launch type, you don't have to provision, configure, or scale clusters of virtual machines to run containers. You just have to specify the CPU and memory requirements for your task, and AWS Fargate launches the containers for you.

- You don't have to provision and maintain the infrastructure
- You don't have to run the `ECS Agent` on the instances
- **It is all serverless**
- AWS just tuns ECS Tasks for your based on the CPU/RAM you need
- To scale, just increase the number of tasks. Simple - no more EC2 instances

## IAM Roles for ECS

### EC2 Instance Profile (EC2 Launch Type only)

- Used bu the `ECS agent`
- Makes API calls to ECS service
- Send container logs to `CloudWatch Logs`
- Pull Docker image from ECR
- Reference sensitive data in `Secrets Manager` or `SSM Parameter Store`

### ECS Task Role

- Allows each task to have a specific role
- Use different roles for different ECS Services you run
- Task Role is defined in the `task definition`

## Load balancer integrations

- `Application Load Balancer` supported and works for most use cases
- `Network Load Balancer` recommended only for high throughput/high performance use cases or to pair it with `AWS Private Link`
- `Classic Load Balancer` is supported but not recommended (no advanced features - no Fargate)

## EFS integration

- You can mount EFS volumes into ECS tasks
- This works for both, EC2 and Fargate launch types
- **Task running in any AZ will share the same data in the EFS file system**
- **Fargate + EFS = serverless**
- **Amazon S3 cannot be mounted as a files system**

## ECS Service Auto Scaling

- Automatically increase/decrease the desired number of ECS tasks
- Amazon ECS Auto Scaling uses `AWS Application Auto Scaling` based on
  - Average CPU utilization
  - Average memory utilization - scale on RAM
  - ALB request count per target - metric coming from the ALB
- `Target tracking` based on the target value for a specific `CouldWatch metric`
- `Step scaling` based on a specified `CloudWatch Alarm`
- `Scheduled scaling` based on a schedule (for predictable changes)
- `Farget Auto Scaling` is much easier to setup (because it is serverless)

### Auto scaling EC2 instances

- Accommodate ECS service scaling by adding underlying EC2 instances
- `Auto Scaling Group Scaling`
  - Scale your ASG based on CPU utilization
  - Add EC2 instances over time
- `EC2 cluster capacity provider`
  - Used to automatically provision and scale the infrastructure for your ECS tasks
  - Capacity provider paired with an Auto Scaling Group
  - Add EC2 instances when you are missing capacity (CPU, RAM, etc)
