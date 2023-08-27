# Modules import

## CommonJS (deprecated)

This is the old way of importing modules in Node.js. It is deprecated and should not be used anymore but you can still find it in old projects.

```javascript
const { foo, bar, baz } = require('placeholders');
```

## ECMAScript modules

It was introduced in ES6 and is the new way of importing modules in `Node.js`. It is the recommended way of importing modules.

```javascript
// Without destructuring
const placeholders = require('placeholders');

// With destructuring
import { foo, bar, baz } from 'placeholders';
```

## Exporting modules

```javascript
// math.js
export const add = (a, b) => a + b;
export const sub = (a, b) => a - b;

// index.js
import { add, sub } from './math.js';
console.log(add(1, 2)); // 3
console.log(sub(1, 2)); // -1

// or, using aliases
import { add as addition, sub as subtraction } from './math.js';
console.log(addition(1, 2)); // 3
console.log(subtraction(1, 2)); // -1
```

## Default export

> You can only have one default export per file.

```javascript
// math.js
const add = (a, b) => a + b;
const sub = (a, b) => a - b;
export default add;
export { sub };

// index.js
import addition from './math.js';
console.log(addition(1, 2)); // 3
```
