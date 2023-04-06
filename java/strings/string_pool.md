# String pool

In large applications, Strings can use a lot of memory. For that reason **Java stores all the *String literals* in the `string pool`**

Remember, only the literals are stored in the `string pool`. The result of an evaluation (except by the `intern()` method) generates a new String

Another important rule is that **compile-time constants are stored in the string pool**

``` java
String foo = "foo";

log.info("{}", foo == "foo");
log.info("{}", foo == "f" + "oo"); // compile-time constant
log.info("{}", foo == "f".concat("oo"));
log.info("{}", foo == " foo".trim());
log.info("{}", foo == new String("foo"));
log.info("{}", foo == new String("foo").intern());
```

> **Output**
> true\
> true\
> false\
> false\
> false\
> true
