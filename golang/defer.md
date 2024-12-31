# `defer`

- Used to delay the execution of a function until the surrounding function returns
- Useful for cleanup actions

```go
func main() {
    file, err := os.Open("example.txt")

    if err != nil {
        fmt.Println("Error opening file:", err)
        return
    }

    defer file.Close()  // Ensures the file is closed when main exits

    fmt.Println("Reading file...")
    // File processing code here
}
```

- **Arguments are evaluated immediately**, although the function call is deferred

```go
i := 5
defer fmt.Println("Deferred with i:", i)
i = 10
fmt.Println("Regular with i:", i)
```

> **Output**\
> Regular with i: 10\
> Deferred with i: 5

- Deferred functions are executed in **LIFO order (Last In, First Out)**

```go
func main() {
    defer fmt.Println("1st Deferred")
    defer fmt.Println("2nd Deferred")
    defer fmt.Println("3rd Deferred")
    
    fmt.Println("Function Body")
}
```

> **Output**\
> Function Body\
> 3rd Deferred\
> 2nd Deferred\
> 1st Deferred

## Using `defer` with `panic` and `recover`

- Deferred functions are executed even if a function panics
- Useful to clean up resources in case of a panic

```go
func main() {
    defer func() {
        if r := recover(); r != nil {
            fmt.Println("Recovered from panic:", r)
        }
    }()

    fmt.Println("Starting main")
    panic("something went wrong")
    fmt.Println("This will not be printed")
}
```

> **Output**\
> Starting main\
> Recovered from panic: something went wrong

## See also

- [defer, panic, and recover](https://go.dev/blog/defer-panic-and-recover)
