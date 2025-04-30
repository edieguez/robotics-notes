# Amazon CloudWatch metrics

Amazon CloudWatch is a monitoring and observability service that provides you with data and actionable insights to monitor your applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health.

It provides metrics for *every* service in AWS. **You can create custom metrics** and **dashboards**

## Terminology

### Metric

Is a variable to monitor, like

- CPU usage
- Network traffic
- Disk I/O
- Custom metrics

> **Metrics have timestamps**

### Namespace

`Metrics` belong to `namespaces`. For example, `AWS/EC2` namespace includes metrics like `CPUUtilization`, `NetworkIn`, `NetworkOut`, etc.

### Dimension

It is an attribute of a `metric`. For example, `InstanceId` is a dimension for the `CPUUtilization` metric. **Up to 30 dimensions per metric**

## CloudWatch metrics streams

Streams metrics to a destination of your choice in **near real-time and low latency**
