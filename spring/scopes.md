# [Spring scopes](https://www.baeldung.com/spring-bean-scopes)

- Singleton
- Prototype
- Request
- Session
- Application
- WebSocket

> All available scopes are present in `ConfigurableBeanFactory`
>
> ``` java
> @Scope(value = ConfigurableBeanFactory.SCOPE_SINGLETON)
> ```

## Singleton

The container creates a single instance of that bean; all requests for that bean name will return the same object which is cached. Any modifications to the object will be reflected in all references to the bean. ==This is the default scope==

## Prototype

Returns a different instance every time it is requested from the container

```java
@Bean
@Scope("prototype")
public Person personPrototype() {
    return new Person();
}
```
