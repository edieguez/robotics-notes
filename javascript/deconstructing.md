# Deconstructing

Allows you to extract values from arrays or objects and assign them to variables in a more concise and readable way.

```javascript
const numbers = [1, 2, 3, 4, 5];
const [first, second, ...rest] = numbers;

console.log(first); // 1
console.log(second); // 2
console.log(rest); // [3, 4, 5]
```

## Object deconstructing

```javascript
const hermit = {
    name: 'Seiga',
    lastname: 'Kaku',
    age: 27
}

// Variable name MUST match the property name
const { name, lastname, age } = hermit;
```

## Nested deconstructing

```javascript
const hermit = {
    name: 'Seiga',
    lastname: 'Kaku',
    age: 27,
    address: {
        street: 'Netherworld',
        number: 666
    }
}

// address won't be defined as a variable. Only street and number will be defined
const { name, lastname, age, address: { street, number } } = hermit;
```
