# Amazon MQ

`SQS` and `SNS` are *cloud native* and proprietary protocols from AWS. Traditional applications that use open protocols may be using

- `MQTT`
- `AMQP`
- `STOMP`
- `OpenWire`
- `WSS`

In such cases, you can use `Amazon MQ` to connect to these applications. `Amazon MQ` is a managed message broker service for Apache `ActiveMQ` and `RabbitMQ`. It supports industry-standard messaging protocols so you can connect to your applications using the protocol that works best for your application

## Caveats when using Amazon MQ

- Does not scale as much as `SQS` or `SNS`
- Runs on servers, that means you can run Multi-AZ with failover
- `Amazon MQ` has both, **queue (SQS) and topic (SNS) capabilities**
