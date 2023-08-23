# Classes

> Under the hood JS does not uses classes. Class syntax is just a syntactic sugar over the prototype-based inheritance.

## Class declaration with constructor

This syntax has been introduced in ES6 (2015)

```js
class Person {
    constructor(name, lastname) {
        this.name = name;
        this.lastname = lastname;
    }
}
```

## Getters and setters

Getters and setters methods are defined using the `get` and `set` keywords respectively. After that, **we can use them as if they were properties**.

```js
class Person {
    constructor(name, lastname) {
        this.name = name;
        this.lastname = lastname;
    }

    get fullName() {
        return `${this.name} ${this.lastname}`;
    }

    set fullName(fullName) {
        const [name, lastname] = fullName.split(' ');
        this.name = name;
        this.lastname = lastname;
    }
}

const person = new Person('John', 'Doe');
console.log(person.fullName); // John Doe

person.fullName = 'Jane Doe';
console.log(person.fullName); // Jane Doe
```
