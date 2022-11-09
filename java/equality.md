# Equality

For comparing two objects you can use `==` or `equals()`

## `==`

Compares object references. If two objects are the same in memory, it will return `true`

``` java
StringBuilder stringBuilderA = new StringBuilder("ABC");
StringBuilder stringBuilderB = new StringBuilder("ABC");
StringBuilder stringBuilderC = stringBuilderA;

log.info("{}", stringBuilderA == stringBuilderB);
log.info("{}", stringBuilderA == stringBuilderC);
```

> **Output**
> false
> true

## `equals()`

**The results may vary**. The default `equals()` method (inherit from `Object`) has exactly the same behavior as the `==` operator. A class can override this method to compare the actual value of the object. One example of this is the [String](strings/String.md) class

``` java
StringBuilder stringBuilderA = new StringBuilder("ABC");
StringBuilder stringBuilderB = new StringBuilder("ABC");
StringBuilder stringBuilderC = stringBuilderA;

log.info("{}", stringBuilderA.equals(stringBuilderB));
log.info("{}", stringBuilderA.equals(stringBuilderC));

String stringA = new String("ABC");
String stringB = new String("ABC");

log.info("{}", stringA == stringB);
log.info("{}", stringA.equals(stringB));
```

> **Output**
> false
> true
> false
> true
