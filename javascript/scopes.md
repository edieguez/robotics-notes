# Scopes

Is the part of the program in which a variable is visible

## Global

Can be referred on any place in the code

## Local

Can only be referred within the block where the variable was defined

## Lexical scoping

A variable defined outside a function can be accessible inside another function defined after the variable declaration

``` javascript
let globalVar = "I'm global";

function outer() {
    let outerVar = "I'm outer";

    function inner() {
        let innerVar = "I'm inner";
        console.log(globalVar); // I'm global
        console.log(outerVar); // I'm outer
        console.log(innerVar); // I'm inner
    }

    inner();
}

outer();
```
