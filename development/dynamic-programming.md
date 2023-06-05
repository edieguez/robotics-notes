# [Dynamic programming](https://www.youtube.com/watch?v=oBt53YbR9Kk)

Dynamic programming is a method for solving a complex problem by breaking it down into a collection of simpler subproblems, solving each of those subproblems just once, and storing their solutions.

1. Make it work
   - Visualize the problem as a `tree`
   - Implement the `tree` using `recursion`

2. Make it efficient
   - Add a `memo object`
   - Add a base case to return `memo values`
   - **Store return values into the memo**

## Fibonacci sequence

### Classic recursive solution

```python
def fib(n):
    if n < 2:
        return n
    return fib(n - 1) + fib(n - 2)
```

### Memoized solution

```python
def fib(n, memo={}):
    if n in memo:
        return memo[n]
    if n < 2:
        return n
    memo[n] = fib(n - 1, memo) + fib(n - 2, memo)
    return memo[n]
```
