# `final` keyword

Java does not support constants in the same way that C does. Instead, it has the `final` keyword, which **can be applied to variables, methods, and classes**. This means that, once defined

- Variables cannot be reassigned
- Methods cannot be overridden, and the c
- Classes cannot be extended.

However, the `final` keyword **does not make variables immutable**. It only means that the variable cannot be reassigned. Therefore **is possible to change the state of an object declared as** `final`.

## `static` blocks

It is possible to assign a variable after its declaration using a [static block](blocks.md#static-block). This is possible because the static block is the first assignment of the variable.

```java
public class GenericClass {
    private static final String name;

    static {
        name = "Generic class";
    }
}
```
