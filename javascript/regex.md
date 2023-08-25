# Regular expressions

> [Regular expressions note](../development/regex.md)

## Basic declaration

```javascript
// Basic form. No modifiers
let longForm = new RegExp('abc');
let shortForm = /abc/;

// Long form with modifiers
let caseInsensitive = new RegExp('abc', 'i'); // i = case insensitive
let global = new RegExp('abc', 'g');          // g = global matching
let multiline = new RegExp('abc', 'm');       // m = multiline matching
let dotAll = new RegExp('abc', 's');          // s = dot matches all
let unicode = new RegExp('abc', 'u');         // u = unicode matching
let sticky = new RegExp('abc', 'y');          // y = sticky matching

// Short form with modifiers
let caseInsensitive = /abc/i; // i = case insensitive
let global = /abc/g;          // g = global matching
let multiline = /abc/m;       // m = multiline matching
let dotAll = /abc/s;          // s = dot matches all
let unicode = /abc/u;         // u = unicode matching
let sticky = /abc/y;         // y = sticky matching
```

## Testing for matches

```javascript
let emailRegex = /[\w.]+@(gmail|outlook|hotmail)\.com/;
let emails = [
  'jhon@gmail.com',
  'jane@outlook.com',
  'nanashi@pishing.com',
]

console.log(emails.filter(email => emailRegex.test(email)))
// → [ 'jhon@gmail', 'jane@outlook' ]
```
