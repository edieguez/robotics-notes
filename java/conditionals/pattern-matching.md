# Pattern matching

Pattern matching is a feature that allows you to match a value against a pattern. It is a more powerful version of the [switch](switch.md) statement in Java. Pattern matching was introduced in Java 14 as a preview feature and became a standard feature in Java 16.

```java
public void patternMatching(Number number) {
    if (number instanceof Integer integer) { // Implicitly casts number to Integer and assigns it to integer
        log.info("Integer: {}", integer);
    } else if (number instanceof Double final doubleValue) { // You can use final to make the variable immutable
        log.info("Double: {}", doubleValue);
    } else {
        log.info("Unknown number type");
    }
}
```

## Subtypes

- The type of the pattern variable **MUST** be a subtype of the type of the expression being matched.
- This rule does not exist for the traditional `instanceof` operator.

```java
Integer value = 123;

if(value instanceof Integer) {}      // Compiles
if(value instanceof Integer data) {} // DOES NOT COMPILE
```

## Flow scoping

Means the variable is only in scope when the compiler can definitively determine the type of the variable. In the following example `integer` is only in scope inside the `if` block.

```java
void printIfInteger(Number number) {
    if (number instanceof Integer integer) {
        log.info(integer); // integer is in scope
    }

    log.info(integer); // DOES NOT COMPILE
}
```

The pattern matching can be inverted by using the `!` operator. In this example `data` is in scope outside the `if` block.

```java
void printIfNotInteger(Number number) {
    if (!(number instanceof Integer data)) {
        return;
    }

    // Compiles although data is defined inside the if block.
    // At this point data is guaranteed to be an Integer so the compiler allows it.
    log.info(data);
}
```
