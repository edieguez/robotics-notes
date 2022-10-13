# [Local variable type inference](https://openjdk.org/projects/amber/guides/lvti-style-guide)

As the name suggest, it **can only be used in local variables**. Therefore it **cannot be used in method/constructor parameters or class/instance variables**

``` java
public class VarKeyword {
    var tricky = "Hello"; // Does not compile

    public void hello(String name) {
        var message = String.format("Hello %s", name); // Valid use
        log.info(message);
    }
}
```

## Type inference

At compile time, Java defines the type of the variable. No matter if you used `var` in its declaration. That means that, once *defined* the type of the variable, it cannot change

This also means it **must be initialized in the same line it is declared**. Also **cannot be used in a multi assignment statement**

``` java
var number = 10;   // Type inference: int
number = 20;       // Type is still int
number = "thirty"; // Invalid. Cannot change from int to String

int a, var b = 3;  // Does not compile
var n = null;      // Does not compile
```

Although `var` cannot be initialized as `null`, it can be assigned `null` once the type has been inferred

``` java
var name = "Seiga Kaku"; // Type inference: String
name = null;             // A String can hold a null value

var age = 27; // Type inference: int
age = null;   // Cannot assign null to a primitive

var kind = (String) null; // Valid statement since the type String can be inferred
```

## `var var`

`var` is not a [reserved word](../keywords.md) but a **reserved type name**. That means it can be used as a variable name but not as a type (`class`, `interface` or `enum` name)

``` java
var var = "var" // Valid statement

...

public class var { // Does not compile
    // Generic code
}
```
