# Variables

- Variables are immutable by default
  - Unless declared with `mut` keyword
  - Alternatively, variables can be *shadowed*

```rust
// Without type annotation
let var = 5;

// With type annotation
let var: i32 = 5;

// Mutable variable without type annotation
let (multi1, multi2) = (5, 6);

// Mutable variable with type annotation
let (multi1, multi2): (i32, i32) = (5, 6);
```

## Using `mut` keyword

```rust
let mut var = 5;

// With type annotation
let mut var: i32 = 5;

// Multiple mutable variables
let mut (multi1, multi2) = (5, 6);

// Multiple mutable variables with type annotation
let mut (multi1, multi2): (i32, i32) = (5, 6);
```

## Constants

- Declared using `const` keyword
- Type annotation is required
- Value must be a *compile time constant*

```rust
const MAX_POINTS: i32 = 100_000;
```
