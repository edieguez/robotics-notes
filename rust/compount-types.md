# Compound types

Rust has two compound types: tuples and arrays.

## Tuples

A tuple is a collection of **values of different types**. Tuples have a fixed length. Once declared, the length cannot be changed.

- Tuples are declared using parentheses `()`
- Elements are separated by commas `,`
- Elements can have different types
- It has a max length of 12

```rust
let tuple = (1, 2.0, "hello");

// With type annotation
let tuple: (i32, f64, &str) = (1, 2.0, "hello");
```

Accessing tuple elements can be done using the **dot notation**.

```rust
let first = tuple.0;
let second = tuple.1;
let third = tuple.2;
```

## Arrays

An array is a collection of **values of the same type**. Arrays have a fixed length. Once declared, the length cannot be changed.

- Arrays are declared using square brackets `[]`
- Elements are separated by commas `,`
- Elements must have the same type
- It has a max length of 32

```rust
let array = [1, 2, 3, 4, 5];

// With type annotation: [type; size]
let array: [i32; 5] = [1, 2, 3, 4, 5];
```

Accessing array elements can be done **using the index**.

```rust
let first = array[0];
let second = array[1];
let third = array[2];
```

## Deconstructing

Both tuples and arrays can be **deconstructed** to access their elements.

```rust
let tuple = (1, 2, 3);
let (a, b, c) = tuple;

let array = [1, 2, 3];
let [a, b, c] = array;

// With type annotation
let (a, b, c): (i32, i32, i32) = tuple;
let [a, b, c]: [i32; 3] = array;
```
