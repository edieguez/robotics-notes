# `async` / `await`

Alternative to [promises](promises.md). Allows to write asynchronous code using synchronous-like code.

```javascript
async function getAdvice() {
    let data = await (
            await fetch('https://api.adviceslip.com/advice')
        ).json();

    return {
        id: data.slip.id,
        advice: data.slip.advice,
    };
}

async function main() {
    let advice = await getAdvice();
    console.log(`[${advice.id}] ${advice.advice}`);
}

main();
```
