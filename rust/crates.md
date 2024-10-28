# Rust crates

> Rust calls dependencies `crates`. You can find crates on [crates.io](https://crates.io).

## Add a crate to your project

1. Edit `Cargo.toml` to add dependencies
2. Look for the `dependencies` section
3. Add the name of the crate you want to use
4. Run `cargo build` to download the crate and build your project

```toml
[dependencies]
rand = "0.8.4"
```

## Using `cargo add`

`cargo add` is a tool that makes adding dependencies easier. You can add a dependency using the following command

```bash
cargo add rand
```

## See also

- [`use` keyword](use.md)
