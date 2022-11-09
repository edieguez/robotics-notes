# [java.lang.StringBuilder](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/StringBuilder.html)

Is a sequence of characters. It implements the interface [CharSequence](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/CharSequence.html). Is similar to [String](String.md) but it **is mutable**

There's also an alternative named [StringBuffer](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/StringBuffer.html). The main difference with this class is that, **`StringBuilder` is thread safe and `StringBuilder` no**

``` java
StringBuilder stringBuilder = new StringBuilder();

for (char i = 'A'; i <= 'z'; i++) {
    if (Character.isAlphabetic(i)) {
        stringBuilder.append(i);
    }
}

log.info("{}", stringBuilder);
```

## Important `StringBuilder` methods

### `charAt()`, `indexOf()`, `length()`, and `substring()`

They behave exactly the same as the methods present in the [String](String.md) class

### `append()`

Add text to the end of the `StringBuilder`. It makes the change in the object itself but also returns the same object (due to the builder pattern)

``` java
StringBuilder stringBuilder = new StringBuilder();

for (char i = 'A'; i <= 'z'; i++) {
    if (Character.isAlphabetic(i)) {
        stringBuilder.append(i);
    }
}

log.info("{}", stringBuilder);
```

> **Output**
> ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz

### `insert()`

Inserts characters at the specified index

``` java
StringBuilder stringBuilder = new StringBuilder("AE");
stringBuilder.insert(1, "BCD");

log.info("{}", stringBuilder);
```

> **Output**
> ABCDE

### delete() and deleteCharAt()

``` java
StringBuilder stringBuilder = new StringBuilder("AremovemeBCXDE");
stringBuilder.delete(1, 9);    // ABCXDE
stringBuilder.deleteCharAt(3); // ABCDE
```

### `replace()`

``` java
StringBuilder stringBuilder = new StringBuilder("Hello planet!");
stringBuilder.replace(6, 12, "world");

log.info("{}", stringBuilder);
```

> **Output**
> Hello world!

### `reverse()`

``` java
StringBuilder stringBuilder = new StringBuilder("ABC");
stringBuilder.reverse();

log.info("{}", stringBuilder);
```

> **Output**
> CBA

### `toString()`

Returns the `String` represented by the StringBuilder object
