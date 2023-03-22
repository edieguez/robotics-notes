# Functional interfaces

These are interfaces that have only one abstract method. They can be annotated with [@FunctionalInterface](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/FunctionalInterface.html) to hint about this. With this annotation, if the rules for functional interfaces are broken, the compiler will throw an error.

A mnemonic for remembering the rules is `SAM` which stands for `Single Abstract Method`. The rules are:

1. The interface must have only one abstract method.
2. The interface can have any number of default methods.
3. The interface can have any number of static methods.
4. The interface can have any number of methods from `java.lang.Object`.

There are four main types of functional interfaces:

1. `Predicate` - takes one parameter and returns a boolean
2. `Consumer` - takes one parameter and returns nothing
3. `Function` - takes one parameter and returns a value
4. `Supplier` - takes no parameters and returns a value

> **Please note that, these are not the only types of functional interfaces. There are many more. These are just the most common ones.**
