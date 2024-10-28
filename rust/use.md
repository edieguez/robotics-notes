# `use` keyword

- Similar to the `import` keyword other languages have
- Used to bring a crate or module into scope
- `std` is the standard library crate
  - It is automatically imported into every Rust program

> lib.rs file

```rust
// pub keyword is used to make the function public
pub fn greeting() {
    println!("Hello, world!");
}
```

> main.rs file

```rust
// my_crate is the name of the package found in Cargo.toml
use my_crate::greeting;

fn main() {
    greeting();
}
```
