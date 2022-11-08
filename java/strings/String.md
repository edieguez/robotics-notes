# [java.lang.String](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/String.html)

Is a sequence of characters. It implements the interface [CharSequence](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/CharSequence.html)

Once a String is created, it **is not allowed to change**

## Concatenation

1. If both operands are numeric, `+` means numeric addition
2. If either operand is a `String`, `+` means concatenation
3. The expression is evaluated left to right
4. `s += "added"` is the same as `s = s + "added"`
