# [Consumer](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/function/Consumer.html)

```java
@FunctionalInterface
public interface Consumer<T> {
    void accept(T t);
}
```

Takes a parameter of type `T` and returns nothing. It is used to perform an action on that object. One example of this could be printing a message to the console.
