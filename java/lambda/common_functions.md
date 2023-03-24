# Common functions

## removeIf()

It is defined in [List](../collections/list.md) and [Set](../collections/set.md) and takes a [Predicate](predicate.md) as parameter. It removes all elements that satisfy the predicate.

```java
...
list.removeIf(s -> s.length() < 5);
```

## sort()

It is an alternative to `Collections.sort()`. It takes a [Comparator](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/Comparator.html) as parameter.

## forEach()

Takes a [Consumer](consumer.md) as parameter. It is defined in [Iterable](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Iterable.html) and [Stream](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/stream/package-summary.html). It goes through all elements and applies the consumer to each of them.
