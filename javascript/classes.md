# Classes

> Under the hood JS does not uses classes. Class syntax is just a syntactic sugar over the prototype-based inheritance.

## Class declaration with constructor

```js
class Person {
    constructor(name, lastname) {
        this.name = name;
        this.lastname = lastname;
    }

    fullName() {
        return `${this.name} ${this.lastname}`;
    }
}
```
