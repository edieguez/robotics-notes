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

## `if` with a short statement

A short statement can be used to declare variables that are only in scope for the `if` block

```go
// Determine if a number is even or odd
if number := 10; number % 2 == 0 {
    fmt.Println("Even")
} else {
    fmt.Println("Odd")
}
```
