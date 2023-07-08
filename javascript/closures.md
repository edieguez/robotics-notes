# Closures

A closure is a function that has access to the parent scope, even after the scope has closed.

``` javascript
function wrapValue(n) {
    let local = n;      // outer scope
    return () => local; // inner scope
}

let wrap1 = wrapValue(1);
let wrap2 = wrapValue(2);

console.log(wrap1()); // 1
console.log(wrap2()); // 2
```

Example of a closure that multiplies by a factor:

``` javascript
function multiplier(factor) {
    return number => number * factor;
}

let twice = multiplier(2);

console.log(twice(5)); // 10
```
