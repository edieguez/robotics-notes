# Creating a JAR file

## Basic usage

``` shell
jar -cvf myProgram.jar .
jar --create --verbose --file myProgram.jar .
jar -cvf myProgram.jar -C dir .
```

## Command line options

- `-c` creates a new JAR file
- `-v` Prints details when working with JAR files
- `-f` JAR filename
- `-C <directory>` Directory containing files to be used to create the JAR
