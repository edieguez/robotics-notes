# Installation

## Environment variables

> This step is optional. You can skip it and use the default installation path

Define these environment variables to customize the installation path

``` shell
export CARGO_HOME=/opt/rust/cargo
export RUSTUP_HOME=/opt/rust/rustup
```

## Installation script

Run the [installation script](https://www.rust-lang.org/tools/install). It will pick up the env variables and use them to store the Rust binaries

``` shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
