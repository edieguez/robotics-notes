# Lambda

They are like anonymous functions. They can be passed as parameters to other methods, assigned to variables and returned from other methods. It uses something called `deferred execution` which means that the code is not executed until it is called.

## Syntax

Lambda expressions can be tricky since many of its elements are optional. If the lambda is expected to return a result, using the short form without curly braces does not require the use of the `return` keyword

```java
// Long form
(ObjectType parameter) -> {
    expression 1;
    expression 2;
    ...
}

(parameters) -> {
    expression 1;
    expression 2;
    ...
}

// Short form
(parameters) -> expression

parameters -> expression

// No parameters
() -> expression
```
