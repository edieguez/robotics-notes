# Scalar types

Rust has a number of built-in scalar types. A scalar type represents a single value. Rust has four primary scalar types

1. Integers
2. Floating-point numbers
3. Booleans
4. Characters

## Integers

Integers are whole numbers. Rust has signed and unsigned integers. Signed integers can be positive or negative. Unsigned integers are always positive.

When defining numbers `_` are allowed to make the number more readable. For example, `1_000` is the same as `1000`.

> `usize` and `isize` are pointer-sized integers. They are 64 bits on a 64-bit architecture and 32 bits on a 32-bit architecture.

| Unsigned | Signed |
|----------|--------|
| u8       | i8     |
| u16      | i16    |
| u32      | i32    |
| u64      | i64    |
| u128     | i128   |
| usize    | isize  |

## Floating-point numbers

Floating-point numbers are numbers with a decimal point. Rust has two floating-point types

1. `f32` - 32-bit floating-point number
2. `f64` - 64-bit floating-point number

## Booleans

- Unlike C or C++, Rust has a dedicated boolean type
- Cannot be converted to integers and vice versa

Allowed values are `true` and `false`. All lowercase.

## Characters

- Rust's `char` type is four bytes in size
- Represents a Unicode Scalar Value
- Enclosed in single quotes

```rust
let c = 'c';

// Declaration with type annotation
let c: char = 'c';
```

## See also

- [Variables](variables.md)
