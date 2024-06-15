# Java compiler

## Basic usage

``` shell
javac Main.java
```

This generates a `Main.class` file that can be executed with `java Main`

## Command line options

- `-d <directory>` directory where the compiled files will be placed
- `-cp <directory>` specify the classpath
- `-classpath <directory>` specify the classpath
- `--class-path <directory>` specify the classpath

> 1. The classpath options can be also used with the `java` command
> 2. To specify multiple directories in the classpath, separate them with `:` in Unix-like systems and `;` in Windows
