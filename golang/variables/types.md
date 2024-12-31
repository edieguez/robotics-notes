# Types

Go is a statically typed language, which means that the type of a variable is known at compile time. The type of a variable determines the values the variable can store and the operations that can be performed on it

- `bool` - a boolean value
- `string` - a sequence of characters
- `int`, `int8`, `int16`, `int32`, `int64` - signed integers
- `uint`, `uint8`, `uint16`, `uint32`, `uint64`, `uintptr` - unsigned integers
- `byte` - alias for `uint8`
- `rune` - alias for `int32`. Represents a Unicode code point
  - When you iterate over a string in Go, you get back `runes`
- `float32`, `float64` - floating point numbers
- `complex64`, `complex128` - complex numbers

## See also

- [Variable declaration](./README.md)
- [Zero values at initialization](./zero-values.md)
- [Constants](./constants.md)
