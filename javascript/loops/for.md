# `for` loop

## Traditional `for` loop

The old and traditional `for` loop we all know and love.

```javascript
for (let i = 0; i < 10; i++) {
  console.log(i); // 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
}
```

## `for...in` loop

Iterates over the keys/indexes of an object, allowing you to access the corresponding values

```javascript
const person = {
  name: 'John',
  age: 30,
  occupation: 'Engineer'
};

for (let key in person) {
  // name: John
  // age: 30
  // occupation: Engineer
  console.log(key + ':', person[key]);
}
```

## `for...of` loop

Iterates over iterable object such as arrays, strings, maps, sets, etc. It provides a simpler syntax and allows you to directly access the values instead of the keys/indexes.

```javascript
const colors = ['red', 'green', 'blue'];

for (let color of colors) {
  console.log(color); // red, green, blue
}
```

## `forEach` method

Although not technically a loop, this method is available on arrays and allows toy to iterate over each element of the array. It takes a callback function as an argument and executes it for each element.

```javascript
const arr = [1, 2, 3, 4, 5];

// Print each element squared
arr.forEach((value) => console.log(Math.pow(value, 2)));
```
