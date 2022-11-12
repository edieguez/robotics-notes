# [YAML Ain't Markup Language](https://yaml.org/spec/1.2.2/)

[YAML Tutorial: Everything You Need to Get Started in Minutes](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started)

> Formerly *Yet Another Markup Language*

The accepted file extensions for this format are `.yaml` and `.yml`

Every yaml file must start with `---`. A single file can contain multiple documents. That means that `---` can appear multiple times to separate all of them

Spaces and indentation are part of the syntax. Like in **Python**

## Comments

Begin with a pound sign `#`

``` yml
---
# This is a full line comment
foo: bar # this is a comment, too
```

## Data types

### Maps

`key: value` pairs. Also know as *dictionaries*. Is the basic building block. Every item in a YAML document is a member of at least one dictionary. **The key is always a `string`** and **the value** is a scalar, so it **can be any datatype**

You can also represent maps in a single line

```yml
---
foo: { foo: Marisa, bar: Patchouli, baz: Alice }
```

### Arrays

You can specify arrays or lists on a single line

```yml
---
items: [ 1, 2, 3, 4, 5 ]
names: [ "one", "two", "three", "four" ]
```

Or you can use the multiline syntax

``` yml
---
items:
  - 1
  - 2
  - 3
  - 4
  - 5
names:
  - "one"
  - "two"
  - "three"
  - "four"
```

### Numeric

Any valid numeric literal is recognized automatically. This includes **decimal** and **floating** literals. Other supported types are **hexadecimal** and **octal**

``` yml
---
foo: 420   # decimal
bar: 0x1A4 # hexadecimal
baz: 0644  # octal
```

Fixed and exponential floating point numbers are supported

```yml
---
 foo: 4.20
 bar: 0.420e+03
```

`Infinity` and `not-a-number (NAN)` are also supported

``` yml
---
foo: .inf  # infinity
bar: -.Inf # negative infinity
plop: .NAN # not-a-number
```

### Strings

Strings are Unicode. In most situations, you don't have to specify them in quotes

You need to specify double quotes `"` when you want to use escape sequences. **If you use single quotes `'` the escape characters won't be interpreted**. Single quotes can be also used if the string contains special characters

``` yml
---
foo: this is a single line
bar: "this is a line\nthis is another line"
baz: 'this is a single line\nwith unescaped characters'
```

You can also use the *fold* character (`>`) to write multiline strings. **It will be returned as a single line when interpreted**

```yml
foo: >
    This is a
    single line
```

To interpret the field as it is you need to use the pipe character `|`

```yml
zen: |
    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
```

### Nulls

``` yml
---
foo: ~
bar: null
```

### Booleans

Accepted values

- **true** `True`, `On` and `Yes`
- **false** `False`, `Off`, or `No`

``` yml
---
foo: True
bar: False
light: On
TV: Off
```
