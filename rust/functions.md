# Function definition

- The convention is to use snake-case for function names
- Since Rust is compiled, functions does not need to appear before the code that uses them

```rust
fn function_name(arg1: Type1, arg2: Type2) -> ReturnType {
    // function body
}

fn sample_function(numA: i32, numB: i32) -> i32 {
    // Implicit return
    // return numA + numB; is also valid but the short form is preferred
    // Note there is not semicolon at the end
    numA + numB
}
```
