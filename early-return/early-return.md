# Early Return

> An early return provides functionality so the result of a conditional statement can be returned as soon as a result is available, rather than wait until the rest of the function is run.

## Example

nested code inside deep `if`s and `else`s seems to make functions a lot harder to follow, and most of the times can be avoided:

```js
function fn(value) {
    if (value !== 0) {
        // ...0
        if (value === 1) {
            // ...1
        } else {
            if (value === 2) {
                // ...2
            } else {
                // ...3
            }
        }
    } else {
        // ...4
    }
}
```

Could be re-written like:

```js
function fn(value) {
    if (value === 0) {
        // ...4
        return;
    }

    // ...0

    if (value === 1) {
        // ...1
        return;
    }

    if (value === 2) {
        // ...2
        return;
    }

    // ...3
}
```

## External Links
[Early Returns in JavaScript](https://dev.to/jenniferlynparsons/early-returns-in-javascript-5hfb)<br/>
[Return early](http://blog.wilsonpage.co.uk/return-early/)<br/>

### Related Patterns
##### `short-circuiting`

[⬅️](https://github.com/Sinakhx/techniques-in-programming#readme)