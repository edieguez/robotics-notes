# [Math](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

## Basic methods and constants

### Math.PI

```js
Math.PI; // 3.141592653589793
```

### Math.abs()

```js
Math.abs(-1); // 1
```

### Math.round()

This method rounds a number to the nearest integer. If the fractional part is -.5 or higher, it rounds up; otherwise, it rounds down.

```js
Math.round(1.5); // 2
Math.round(1.4); // 1
```

### Math.floor()

Rounds a number down to the nearest integer. It always rounds towards negative infinity. **Negative numbers stay negative**

```js
Math.floor(1.5); // 1
Math.floor(-42); // -42
```

### Math.ceil()

Rounds a number up to the nearest integer. It always rounds towards positive infinity. **Negative numbers stay negative**

```js
Math.ceil(1.5); // 2
Math.ceil(-42); // -42
```

### Math.random()

Returns a random number between 0 (inclusive) and 1 (exclusive).

```js
// Common pattern to generate a random integer within a specified range [min, max]
let random = Math.floor(Math.random() * (max - min + 1)) + min;
```

### Math.pow()

Returns the base to the exponent power, that is, base^exponent.

```js
Math.pow(2, 3); // 8
```
