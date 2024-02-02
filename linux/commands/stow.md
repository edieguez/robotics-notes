# [GNU stow](https://www.gnu.org/software/stow/manual/stow.html)

> Utility to manage dotfiles in a single repository

1. A `package` is a directory within the `.dotfiles` directory containing the configuration files for a specific program
2. If `--target` is not specified, the `target` directory is the parent directory of the `.dotfiles` directory
3. Use `--simulate --verbose=1` to see what would be done without actually doing it

> [YouTube video for simple setup and usage](https://www.youtube.com/watch?v=y6XCebnB9gs)

## `package` to `target`

```bash
stow --verbose=1 $package
```

## `target` to `package`

> To `adopt` a `package`, the `target` directory must contain the configuration files for the `package`. No matter is they are empty or not.

```bash
stow --verbose=1 --adopt $package
```
