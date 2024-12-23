# `if` statement

The `if` statement is used to execute a block of code only if a specified condition is true

1. Does not allow evaluating the truthiness of a value
2. Conditions does not require parentheses
   - Therefore `1` is not considered `true` and `0` is not considered `false`

```go
// Determine if a number is even or odd
number := 10

if number % 2 == 0 {
    fmt.Println("Even")
} else {
    fmt.Println("Odd")
}
```
