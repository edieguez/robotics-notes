# `for` loop

The `for` loop is the only loop statement in Go. It has three forms:

1. `for` loop with a single condition. Similar to a `while` loop
2. `for` loop with a traditional initial/condition/after structure.
3. `for` each loop. Similar to a `foreach` loop in other languages.
4. Infinite loop

## `for` loop with a single condition

The loop will continue as long as the `condition` is `true`

```go
i := 0

for i < 5 {
    fmt.Println(i)
    i++
}
```

## `for` loop with a traditional initial/condition/after structure

The loop will continue as long as the `condition` is `true`. The `initial` statement is executed before the first iteration. The `after` statement is executed after each iteration.

```go
for i := 0; i < 5; i++ {
    fmt.Println(i)
}
```

## `for` each loop

The loop will iterate over each element of the `range` and execute the block of code

- You can use `_` to ignore the index or value

```go
a := []int{1, 2, 3}

for i, value := range a {
    fmt.Println(i, value)
}
```

## Infinite loop

The loop will continue indefinitely

```go
for {
    fmt.Println("Infinite loop")
}
```
