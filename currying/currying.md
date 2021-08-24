# Currying
*Wikipedia:*

> Currying is the technique of converting a function that takes multiple arguments into a sequence of functions that each takes a single argument.<br/><br/>For example, currying a function ***f*** that takes three arguments creates three functions.<br/>***x = f(a, b, c)*** becomes:<br/>***h = g(a)***<br/>***i = h(b)***<br/>***x = i(c)***<br/>or called in sequence:<br />***x = g(a)(b)(c)***

## Example

A function that adds two numbers *without* currying:

```js
    function add (a, b) {
        return a + b;
    }

    add(3, 4); // returns 7
```

A function that adds two numbers *with* currying:

```js
    function add (a) {
        return function (b) {
            return a + b;
        }
    }

    add(3)(4); // returns 7
```

or a simpler syntax could be:

```js
    const add = a => b => a + b;
    add(3)(4); // returns 7
```

## External Links
[wikipedia](https://en.wikipedia.org/wiki/Currying)<br/>
[stackoverflow](https://stackoverflow.com/questions/36314/what-is-currying)<br/>

### Related Patterns
##### `HOF`, `closure`

[⬅️](https://github.com/Sinakhx/techniques-in-programming#readme)