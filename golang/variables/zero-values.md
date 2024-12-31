# Zero values at initialization

Variables in Go are initialized with a zero value if no value is specified. The zero value is the default value of the variable's type. The zero value of a variable is the value that the variable would have if it were declared without an explicit value

- `bool`: `false`
- `string`: `""`
- `int`, `int8`, `int16`, `int32`, `int64`: `0`
- `uint`, `uint8`, `uint16`, `uint32`, `uint64`, `uintptr`: `0`
- `byte`: `0`
- `rune`: `0`
- `float32`, `float64`: `0`
- `complex64`, `complex128`: `0 + 0i`
- `array`: `[0]`
- `slice`: `nil`
- `map`: `nil`
- `channel`: `nil`
- `pointer`: `nil`
- `function`: `nil`
- `interface`: `nil`
- `struct`: `nil`

## See also

- [Variable declaration](./README.md)
- [Types](./types.md)
