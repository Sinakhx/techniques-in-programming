# Flag

> A flag variable, in its simplest form, is a variable you define to have one value until some condition is true, in which case you change the variable's value. It is a variable you can use to control the flow of a function or statement, allowing you to check for certain conditions while your function progresses.

## Example

to check if a condition meets (like counting errors):

```js
    // errors is the flag variable
    var errors = 0;

    for(var i = 0; i < 10; i++) {
        if(i == 6) {  // Your error condition
            errors++;
        }
    }

    if(errors) {  // Is the flag "up"? (i.e. > 0)
        alert("There was a problem!");
    }
```

to check if the given array has an even number:

```js
function hasEven(arr){
    let flag = false;
    for (let i = 0; i < arr.length; i++){
        if (arr[i] % 2 == 0){
            flag = true;
            break;
        }
    }
    return flag;
}
const arr = [1, 3, 2, 5, 6, 7]; 
if (hasEven(arr)){
    console.log("Yes!");
} else {
    console.log("No!");
}

```

## External Links
[javascriptkit](http://www.javascriptkit.com/javatutors/valid2.shtml)<br/>
[stackoverflow](https://stackoverflow.com/questions/17402125/what-is-a-flag-variable)
[geeksforgeeks](https://www.geeksforgeeks.org/use-of-flag-in-programming/)

### Related Patterns
##### `state`

[⬅️](https://github.com/Sinakhx/techniques-in-programming#readme)