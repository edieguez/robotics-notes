# [Elastic Load Balancing (ELB)](https://aws.amazon.com/elasticloadbalancing)

Load balancer. Can scale up and down automatically based on incoming traffic and distribute traffic across multiple instances.

- Integrates with [EC2](ec2.md), [ECS](ecs.md) and [Lambda](lambda.md)
  1. Application Load Balancer
  2. Network Load Balance
  3. Classic Load Balance

## Scaling types

1. `Vertical scaling` increase the size of the instance. AKA `scale up`
2. `Horizontal scaling` increase the number of instances. AKA `scale out`
