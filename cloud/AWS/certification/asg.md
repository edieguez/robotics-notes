# Auto Scaling Groups

- `Scale out` aka `horizontal scaling` add more EC2 instances
- `Scale in` aka `vertical scaling`
- Ensure to have a `minimum` and `maximum` number of instances
- Automatically register new instances to load balancer. There is also a `desired instances` param
- Recreate EC2 if instances is unhealthy
- Can scale out based on CloudWatch alarms

## Scaling policies

- `Dynamic scaling`
  - Target tracking scaling
  - Simple/step scaling
- `Scheduled scaling`
  - Anticipate scaling based on known usage patterns
- `Predictive scaling` forecast load and schedule scaling ahead

## Sample metrics to scale on

- CPU utilization
- Memory utilization
- Request count per target
- Average network in/out
- Any custom metric push to CloudWatch

## Scaling cooldowns

- After scaling  you are in a `cooldown period`
- **It defaults to 300 seconds**
- In this period, launch and termination is paused to stabilize metrics
