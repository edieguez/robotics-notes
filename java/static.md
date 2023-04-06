# `static` keyword

> Also refer to the [blocks](blocks.md) note

`static` methods and variables belong to the class itself. They're not bound to any instance of the class

They can be used for

- Utility or helper methods that don't need to access instance variables (a.k.a. keep an state)
- An state that is shared across all instances of the class. E.g. a counter that keeps track of how many instances of the class have been created

`static` methods and variables are accessed through the class name, not through an instance of the class. *It can be done using an instance variable, but it's not recommended*
