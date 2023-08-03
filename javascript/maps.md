# Maps

A map is a collection of key-value pairs. A key can be any value, but it must be unique. A value can be any value, and it can be repeated.

``` javascript
// Formal form
const hermit = new Map();
hermit.set('name', 'Seiga');
hermit.set('age', 27);

// Short form
const hermit = {
  name: 'Seiga',
  age: 27
};

// Implicit form: the keys are variable and the values are the variables' values
const name = 'Seiga';
const age = 27;

const hermit = {name, age};
```
