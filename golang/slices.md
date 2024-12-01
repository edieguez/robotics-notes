# Arrays and slices

- `array` is a **fixed-size** sequence of elements of the same type
- `slice` is a **dynamically-sized** sequence of elements of the same type

## Creating arrays

> Once an array is created, its size is fixed. It cannot be changed

```go
// Array of 5 integers
var a [5]int

// Array with predefined values
b := [3]int{1, 2, 3}
```

## Creating slices

> When a slice is created, it points to an underlying array

```go
// Slice of integers
var s []int

// Slice with predefined values
t := []int{1, 2, 3}
```

## See also

- [Go Slices: usage and internals](https://go.dev/blog/slices-intro)
