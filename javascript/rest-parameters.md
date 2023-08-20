# Rest parameters

Rest parameters are used to create functions that accept any number of arguments.

```javascript
function calculateSum(...numbers) {
  let sum = 0;

  for (let num of numbers) {
    sum += num;

  }
  return sum;
}

const result = calculateSum(2, 4, 6, 8);

console.log(result); // This will output 20
```

Tiple dot notation `...` can be used to *spread* an array into individual elements.

```javascript
const numbers = [2, 4, 6, 8];
const result = calculateSum(...numbers); // Spread the array into individual elements

console.log(result); // This will output 20
```
