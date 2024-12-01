# Arrays

It is a fixed-size collection of items of the same type

1. Size is determined at creation time
2. After creation, the **size cannot be changed**
3. Type of items is also determined at creation time

```go
var a [3]int // Simple initialization

// Assigning values
a[0] = 1
a[1] = 2
a[2] = 3

// Short initialization
b := [3]int{1, 2, 3}

// Letting the compiler determine the size
c := [...]int{1, 2, 3}

// Partial initialization
// Uninitialized elements are set to 0 (or default value depending on the type)
d := [5]int{1, 2, 3}
```

## Common Operations

```go
a := [3]int{1, 2, 3}

// Accessing elements
fmt.Println(a[0]) // 1

// Length of the array
fmt.Println(len(a)) // 3

// Iterating over the array
for i, value := range a {
    fmt.Println(i, value)
}
```

## Slicing

```go
a := [5]int{1, 2, 3, 4, 5}

// Creating a slice from 1 (inclusive) to 3 (exclusive)
b := a[1:3] // [2 3]
```

## Copying Arrays

```go
a := [3]int{1, 2, 3}
b := a // b is a copy of a

// Changing b does not affect a
b[0] = 4

fmt.Println(a) // [1 2 3]
fmt.Println(b) // [4 2 3]
```
