# Primitive types

> All the numeric types are signed in Java. That means they range goes from a negative number to a positive

| Keyword   | Type                        | Range                                                                                                              |
|-----------|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| `boolean` | true or false               | true or false                                                                                                      |
| `byte`    | 8-bit integral value        | -128 ... 127<br>-2^⁷ ... 2^⁷ -1<br>Byte.MIN_VALUE ... Byte.MAX_VALUE                                               |
| `short`   | 16-bit integral value       | −32,768 ... 32,767<br>−2^15 ... 2^15 −1<br>Short.MIN_VALUE ... Short.MAX_VALUE                                     |
| `int`     | 32-bit integral value       | −2,147,483,648 ... 2,147,483,647<br>−2^31 ... 2^31 −1<br>Integer.MIN_VALUE ... Integer.MAX_VALUE                   |
| `long`    | 64-bit integral value       | −9,223,372,036,854,775,808 ... 9,223,372,036,854,775,807<br>−2^63 ... 2^63 −1<br>Long.MIN_VALUE ... Long.MAX_VALUE |
| `float`   | 32-bit floating-point value | approximately ±3.40282347E+38F<br>(6-7 significant decimal digits)<br>Java implements IEEE 754 standard            |
| `double`  | 64-bit floating-point value | approximately ±1.79769313486231570E+308<br>(15 significant decimal digits)                                         |
| `char`    | 16-bit Unicode value        | 0 to 65,536                                                                                                        |

## Default types

- `int` is the default type for an integral literal
- This behavior can be overridden adding an `l`/`L` at the end of the number. i.e. `123L` will create a `long` value

## Alternative notations

``` java
int bin = 0B10;
int oct = 017;
int hex = 0xFF;

log.info("binary: {}", bin);
log.info("octal: {}", oct);
log.info("hexadecimal: {}", hex);
```

> **Output**\
> binary: 2\
> octal: 15\
> hexadecimal: 255
