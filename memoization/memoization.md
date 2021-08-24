# Memoization
*Wikipedia:*

> Memoization is an optimization technique used primarily to speed up computer programs by storing the results of expensive function calls and returning the cached result when the same inputs occur again.

## Example

The [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_number) without memoization:

```js
    function Fib(n) {
        if (n < 2) return n;
        return Fib(n - 1) + Fib(n - 2);
    }

    Fib(3); // -> 2
    Fib(4); // -> 5
```

The Fibonacci sequence by adding memoization:

```js
    const Fib = (() => {
        const cache = [1, 1];
        const fib = (n) => {
            if (n >= cache.length) {
                for (let i = cache.length; i <= n; i++) {
                    cache[i] = cache[i - 2] + cache[i - 1];
                }
            }
            return cache[n];
        }
        return fib;
    })();
    
    Fib(3); // -> 2
    Fib(4); // -> 5
```

## External Links
[wikipedia](https://en.wikipedia.org/wiki/Memoization)<br/>
[Memoization in JavaScript](https://keith.gaughan.ie/javascript-memoization.html)<br/>

### Related Patterns
##### `iife`, `closure`, `HOF`

[⬅️](https://github.com/Sinakhx/techniques-in-programming#readme)