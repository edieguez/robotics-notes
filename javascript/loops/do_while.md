# `do... while` loop

Iterates over a block of code while a condition is true. The difference between this and the [while](./while.md) loop is that the `do...while` loop will always execute the code block at least once, even if the condition is false.

```javascript
let i = 0;

do {
  // This block is guaranteed to run at least once
  console.log(i); // 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
  i++;
} while (i < 10);
```
