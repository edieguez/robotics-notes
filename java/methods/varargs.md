# varargs

They can be used as a method parameter to express that method accepts a variable number of arguments of the same type.

1. You can only have one varargs parameter per method
1. The varargs parameter must be the last parameter in the method declaration

```java
// Alternative main method declaration. The type of args is String[]
public static void main(String... args) {
    log.info("{}", sum(1, 2, 3, 4, 5));
}
```
