# instanceof

Cannot be used with incompatible types

``` java
public static void openZoo(Number time) {
    if (time instanceof String) { // Does no compile
        // Code stub
    }
}
```

This rule only applies to classes, but not interfaces

## `null` and the instanceof operator

Since `null` itself is not a type, it cannot be used as the second operand of `instanceof`

``` java
log.info(null instanceof String); // Ok code
log.info(object instanceof null)  // Does not compile
log.info(null instanceof null)    // Does not compile
```
