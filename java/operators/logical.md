# Logical operators

| Operator   | Description                                                 |
|:----------:|-------------------------------------------------------------|
| &          | `true` if both values are `true`                            |
| \|         | `true` if at least one of the values is `true`              |
| ^          | `true` only if one value is `true` and the other is `false` |

## Short-circuit operators

Both, `&&` and `||` are also valid operators. The difference is that, if the expression result can be determined evaluating the first operand, the second one never gets evaluated

``` java
// Second expression is not evaluated if object is null
if (object != null && object.getValue() > 10) {
    // Do something nice here
}
```

## XOR logic table

|                 | Y = `true` | Y = `false` |
|:---------------:|:----------:|:-----------:|
| **Y = `true`**  | `false`    | `true`      |
| **Y = `false`** | `true`     | `false`     |
