# Generators

They are a type of function used to `yield` values. They are defined with the `function*` syntax.

```javascript
function* range(start, end) {
    for (let i = start; i <= end; i++) {
        yield i;
    }
}

for (let i of range(1, 5)) {
    console.log(i);
}
```
