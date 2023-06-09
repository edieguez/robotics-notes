# `static` keyword

> Also refer to the [blocks](blocks.md#static-block) note

`static` methods and variables belong to the class itself. They're not bound to any instance of the class

They can be used for

- Utility or helper methods that don't need to access instance variables (a.k.a. keep an state)
- An state that is shared across all instances of the class. E.g. a counter that keeps track of how many instances of the class have been created

`static` methods and variables are accessed through the class name, not through an instance of the class. *It can be done using an instance variable, but it's not recommended*

## `static` imports

> See also [imports](imports.md)

`static` imports allow you to use `static` methods and variables without having to prefix them with the class name. A normal import does not include static members

```java
// Import PI constant and random() method. This also works with static classes
import static java.lang.Math.PI;
import static java.lang.Math.random;
```
