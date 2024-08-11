# AWK cheat sheet

AWK (Aho, Weinberger, and Kernighan) is a programming language and utility included in Unix-like operating systems for text processing and typically used as a data extraction and reporting tool.

## Basic usage

```bash
# Matches pattern and executes action on file
awk 'pattern { action }' file

# No pattern, executes action on every line
awk '{ action }' file

# No action, prints every line
awk 'pattern' file
```

## Variable declaration

```bash
# Declare variable
awk '{ var = value }' file

# Declare array
awk '{ array[1] = value }' file
awk '{ line[NR] = $0 }' file  # remember each input line

# Declare multiple variables
awk '{ var = value; var2 = value2 }' file

# Increment variable
awk '{ var++ }' file
```

## Control structures and loops

```bash
# If statement
awk '{ if (condition) { action } }' file

# If-else statement
awk '{ if (condition) { action } else { action } }' file

# While loop
awk '{ while (condition) { action } }' file

# For loop
awk '{ for (i = 1; i <= 10; i++) { action } }' file
```

## `BEGIN` and `END` blocks

```bash
# Execute action before processing file
awk 'BEGIN { action } { print $0 }' file

# Execute action after processing file
awk '{ print $0 } END { action }' file
```

## Build-in functions

```bash
# Print number of lines
awk 'END { print NR }' file

# Print number of fields
awk '{ print NF }' file

# Length of string
awk '{ print length($1) }' file
```

## Regular expressions

```bash
# Print lines that match pattern
awk '/pattern/' file

# Print lines that do not match pattern
awk '!/pattern/' file

# Print lines where field matches pattern
awk '$1 ~ /pattern/' file

# Print lines that match pattern1 and pattern2
awk '/pattern1/ && /pattern2/' file

# Print lines that match pattern1 or pattern2
awk '/pattern1/ || /pattern2/' file
```

## `printf` function

```bash
# Print formatted output
awk '{ printf "Name: %s, Age: %d\n", $1, $2 }' file

# Print formatted output with field width
awk '{ printf "Name: %10s, Age: %3d\n", $1, $2 }' file

# Print formatted output with left alignment
awk '{ printf "Name: %-10s, Age: %3d\n", $1, $2 }' file

# Print formatted output with leading zeros
awk '{ printf "Name: %010s, Age: %03d\n", $1, $2 }' file

# Print formatted output with floating point number
awk '{ printf "Name: %s, Age: %d, Height: %.2f\n", $1, $2, $3 }' file
```
