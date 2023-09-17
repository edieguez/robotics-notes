# `switch` statement

The `switch` statement is used to perform different actions based on different conditions.

```javascript
switch (expression) {
  case value1:
    // code block to be executed if expression === value1
    break;
  case value2:
    // code block to be executed if expression === value2
    break;
  default:
    // code block to be executed if expression is different from both value1 and value2
}
```

1. `expression` is evaluated once. The value of the expression is compared with the values of each `case`. If there is a match, the associated block of code is executed.
2. `default` specifies some code to run if there is no case match. If `default` is not included, and no case matches, no code will be executed.
