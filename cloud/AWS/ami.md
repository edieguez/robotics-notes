# Amazon Machine Image (AMI)

Template for an EC2 instance. Includes configuration (OS, application server, applications, etc), launch permissions, and block device mapping.

There's a public repository (or market) of AMIs. You can also create your own AMI and share it with other AWS users.

## AMI types

- `On-demand` - pay for what you use
- `Reserved` - pay for a reserved instance for a period of time
- `Saving Plans` - pay for a commitment to use a specific amount of compute power for a period of time
- `Spot` - bid for unused EC2 instances
- `Dedicated` - pay for a physical server

### On-demand

Provides discounts if you sign a contract to keep that instance running X amount of time (1 up to 3 years).

- `Standard` - up to 75% discount. Highest discount
- `Convertible` - up to 54% discount. Can change the instance type
- `Scheduled` - up to 72% discount. Runs on a schedule. For predictable workloads

### Spot

Can provide up to 90% savings compared to `on-demand` pricing. There is a market place on each availability zone where you can bid for unused EC2 instances. If your bid is higher than the asking price, your instance will be launched. If the spot price goes above your bid, your instance will be terminated within two minutes.
