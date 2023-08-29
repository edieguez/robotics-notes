# Promises

Is an object representation of the eventual completion (or failure) of an asynchronous operation, and its resulting value.

- Additional arguments for the `resolve` and `reject` functions will be ignored
- The promise must have the logic to call either `resolve` or `reject`
- `resolve` and `reject` will be handled by the `then` and `catch` methods respectively
- `finally` is optional and will be called regardless of the promise being resolved or rejected

```javascript
let promise = new Promise((resolve, reject) => {
    let shouldResolve = Math.random() > 0.5;

    if (shouldResolve) {
        resolve('Success!');
    } else {
        reject('Failure!');
    }
});

promise.then((success) => {
    console.log(success);
}).catch((failure) => {
    console.log(failure);
}).finally(() => {
    console.log('Done!');
});
```
