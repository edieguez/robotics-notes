# Numeric promotion

1. If two values have different data types, Java will automatically promote one of the values to the larger of the data types
2. If one of the values is integral and the other is floating-point, Java will automatically promote the integral value to the floating-point value's data type
3. Smaller data types, namely, `byte`, `short`  and `char` are first promoted to `int` any time they're used with Java binary arithmetic operator, even if neither of the operands is `int`
4. After all promotion has occurred and the operands have the same data type, the resulting value will have the same data tye as its promoted operands

## Complex operators implicit casting

A complex operator performs a casting to fit the result into the target variable

``` java
long a = 10;
int b = 5;
b = a * b; // Assigning long to int. Does not compile

long a = 10;
int b = 5;
b *= a; // Automatic casting to int. Result is 50
```

## Ternary operator and promotion

- It can return a `boolean`, `numeric` or `reference`
- For `boolean` and `numeric` categories the result is a primitive
- ==Unboxing occurs when using wrappers==

## Numeric conditional expression type

- The type will be `primitive`
- The type will be the smallest type that reliably holds the result
  - That's the oposite from promotion
  - `byte : short` produces a `short`, not an `int`
  - ==This only happens when no arithmetics in involved==. Otherwise promotion will be applied
  - Constant expressions of exactly `int` can be fit into smaller types if the other argument is suitable
