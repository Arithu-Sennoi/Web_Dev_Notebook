using `\w` is same as using `[a-zA-Z0-9_]`. It will match all letters of both cases, numericals, and also underscore. 
To match all stuff that isn't these things, we use `\W`. It is same as using `[^a-zA-Z0-9_]`. So it will match charecters that isn't any of these. 
Look at this example: 
```js
let testString = "This is a cool_string. It has number 100 in it."
let myRegex = /\w/g;
let result = testString.match(myRegex);
console.log(result);
```
We used `g` flag here, because we want to get all charecters that match the pattern. The console would have an array with all charecters in `testString` printed out. 

To match only numericals, use `\d`. It is same as using `[0-9]`. To have anything but numericals, use `\D`. It is same as using `\[^0-9]\`. 