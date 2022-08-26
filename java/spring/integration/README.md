# [Spring integration](https://spring.io/projects/spring-integration)

Is a way to integrate the [EIP](../../../wiki/dictionary/eip.md) in Spring. It shares some concepts and ideas with [JMS](../../../wiki/dictionary/jms.md)

- **Producer (sender)** is an *endpoint* in Spring integration
- **Consumer (receiver)** is an *endpoint* in Spring integration
- **Pipe** is called *channel* in Spring integration

## [Message endpoints](https://docs.spring.io/spring-integration/docs/5.1.0.RELEASE/reference/html/overview.html#overview-endpoints)

- **[Channel adapter](https://docs.spring.io/spring-integration/docs/5.1.0.RELEASE/reference/html/overview.html#overview-endpoints-channeladapter)** connect your channel to another system
- **[Message transformer](https://docs.spring.io/spring-integration/docs/5.1.0.RELEASE/reference/html/overview.html#overview-endpoints-transformer)** convert message content or structure
- **Enricher** adds content to the message header or payload
- **[Service activator](https://docs.spring.io/spring-integration/docs/5.1.0.RELEASE/reference/html/overview.html#overview-endpoints-service-activator)** invokes service operations when a new message arrives
- **Gateway** connect your channels without [SI](../../../wiki/dictionary/si.md) coupling

## [Message channels](https://docs.spring.io/spring-integration/docs/5.1.0.RELEASE/reference/html/messaging-channels-section.html)

They have two general classifications

1. [Pollable channel](https://docs.spring.io/spring-integration/docs/5.1.0.RELEASE/reference/html/messaging-channels-section.html#channel-interfaces-pollablechannel)
2. [Subscribable channel](https://docs.spring.io/spring-integration/docs/5.1.0.RELEASE/reference/html/messaging-channels-section.html#channel-interfaces-subscribablechannel)
