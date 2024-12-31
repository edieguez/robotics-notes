# `switch` statement

The `switch` statement is a multi-way branch statement. It provides a clean way to write multiple `if-else` statements

- Evaluates the expression and compares it with the values of the `case` clauses
- If a match is found, the statements in the corresponding `case` clause are executed
- If no match is found, the statements in the `default` clause are executed
  - `default` clause is optional
- Unlike other languages, Go does not require a `break` statement at the end of each `case` clause
  - The `break` statement is implicit
  - To fall through to the next `case` clause, use the `fallthrough` statement
- Multiple expressions can be evaluated in a single `case` clause by separating them with a comma

```go
func isVowel(c rune) bool {
    switch c {
    case 'a', 'e', 'i', 'o', 'u':
        return true
    default:
        return false
    }
}
```

## `switch` **without** expression

- If the `switch` statement does not have an expression, it behaves like an `if-else` statement
- `case` statements can contain expressions

```go
func isVowel(c rune) bool {
    switch {
    case c == 'a', c == 'e', c == 'i', c == 'o', c == 'u':
        return true
    default:
        return false
    }
}
```
