```js
// method chaining = calling one method after another 
// in one continuous line of code 
let userName = "bro"; 
let letter = userName.charAt(0).toUpperCase(); 
console.log(letter);
```

You could continuously call functions(methods) one after another, seperated by a dot. It would execulte them, one by one in the order they were written. So here, it would first perform chatAt() function first, then toUpperCase() function next. You can have as many methods as you like, chained like this. 