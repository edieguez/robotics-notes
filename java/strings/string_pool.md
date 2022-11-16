# String pool

In large applications, Strings can use a lot of memory. For that reason **Java stores all the *String literals* in the `string pool`**

Remember, only the literals are stored in the `string pool`. The result of an evaluation (except by the `intern()` method) generates a new String

Another important rule is that **compile-time constants are stored in the string pool**

``` java
String foo = "foo";

log.info("{}", fooA == "foo");
log.info("{}", fooA == "f" + "oo"); // compile-time constant
log.info("{}", fooA == "f".concat("oo"));
log.info("{}", fooA == " foo".trim());
log.info("{}", fooA == new String("foo"));
log.info("{}", fooA == new String("foo").intern());
```

> **Output**
> true
> true
> false
> false
> false
> true
