# Promises

> See also [async/await](async-await.md)

Is an object representation of the eventual completion (or failure) of an asynchronous operation, and its resulting value.

- Additional arguments for the `resolve` and `reject` functions will be ignored
- The promise must have the logic to call either `resolve` or `reject`
- `resolve` and `reject` will be handled by the `then` and `catch` methods respectively
- You can chain multiple `then` statements
- `finally` is optional and will be called regardless of the promise being resolved or rejected

```javascript
let advice = () => {
    return new Promise((resolve, reject) => {
        fetch('https://api.adviceslip.com/advice')
            .then(response => response.json())
            .then(response => resolve({
                id: response.slip.id,
                text: response.slip.advice
            }))
            .catch((error) => reject(error));
    });
};

advice()
    .then(advice => console.log(`[${advice.id}] ${advice.text}`))
    .catch(error => console.log(error))
    .finally(() => console.log('Promise has been settled'));
```
