# [Function](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/function/Function.html)

```java
@FunctionalInterface
public interface Function<T, R> {
    R apply(T t);
}
```

It is used to transform a value of type `T` into a value of type `R`. One example of this could be converting a `String` to an `Integer`.
