# Lists

## Basic declaration

``` javascript
const fruits = ['apple', 'banana', 'orange']
```

## Common methods

### `push`

Add new elements at the end of the list

``` javascript
const fruits = ['apple', 'banana', 'orange']
fruits.push('strawberry') // ['apple', 'banana', 'orange', 'strawberry']
```

### `pop`

Remove the last element of the list

``` javascript
const fruits = ['apple', 'orange', 'banana']
let last = fruits.pop()

console.log(fruits) // ['apple', 'orange']
console.log(last)   // 'banana'
```

### `shift`

Removes and returns the first element of the list

``` javascript
const fruits = ['apple', 'banana', 'orange'];
const firstFruit = fruits.shift();

console.log(fruits);     // ['banana', 'orange']
console.log(firstFruit); // 'apple'
```

### `unshift`

Add new elements at the beginning of the list and returns the new length of the list

``` javascript
const fruits = ['apple', 'banana', 'orange'];
const newLength = fruits.unshift('strawberry');

console.log(fruits);    // ['strawberry', 'apple', 'banana', 'orange']
console.log(newLength); // 4
```

### `slice`

Returns a new list with the elements between the start (inclusive) and end indexes (exclusive)

``` javascript
const fruits = ['apple', 'banana', 'orange', 'strawberry', 'kiwi'];
const subList = fruits.slice(1, 3);

console.log(subList); // ['banana', 'orange']
```

### `splice`

Changes the content of a list by removing existing elements and/or adding new elements. Unlike `slice`, this method **mutates the original list and the indexes are inclusive**.

``` javascript
const fruits = ['apple', 'banana', 'orange', 'strawberry', 'kiwi'];
const removed = fruits.splice(1, 2, 'pear', 'grape');

console.log(fruits);  // ['apple', 'pear', 'grape', 'strawberry', 'kiwi']
console.log(removed); // ['banana', 'orange']
```

### `concat`

Returns a new list resulting from the concatenation of the original list with the given lists

``` javascript
const fruits = ['apple', 'banana'];
const vegetables = ['tomato', 'potato'];
const fruitsAndVegetables = fruits.concat(vegetables);

console.log(fruitsAndVegetables); // ['apple', 'banana', 'tomato', 'potato']
```

### `join`

Joins all elements of an array into a string, with an optional separator. If no separator is provided, a comma is used by default.

``` javascript
const fruits = ['apple', 'banana', 'orange'];
const fruitsString = fruits.join(', ');

console.log(fruitsString); // 'apple, banana, orange'
```

### `reverse`

Reverses the order of the elements of the list. It **mutates the original list**.

``` javascript
const fruits = ['apple', 'banana', 'orange'];
fruits.reverse();

console.log(fruits); // ['orange', 'banana', 'apple']
```

### `sort`

Sorts the elements of the list. It **mutates the original list**.

``` javascript
const fruits = ['orange', 'banana', 'apple'];
fruits.sort();

console.log(fruits); // ['apple', 'banana', 'orange']
```

### `map`

Crates a new array with the results of calling a provided function on every element in the array.

``` javascript
const numbers = [2, 3, 4, 5]
const squared = numbers.map((number) => Math.pow(number, 2))

console.log(numbers) // [2, 3, 4, 5]
console.log(squared) // [4, 9, 16, 25]
```

### `filter`

Creates a new array with all elements that pass a certain condition

``` javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const evenNumbers = numbers.filter((number) => number % 2 === 0);

console.log(evenNumbers); // [2, 4, 6, 8, 10]
```
