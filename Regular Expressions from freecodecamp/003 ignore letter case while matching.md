While matching strings, you may want to match it even when the letter case is different. 
You can match both cases using what is called a flag. There are other flags but here you'll focus on the flag that ignores case - the `i` flag. You can use it by appending it to the regex. An example of using this flag is `/ignorecase/i`. This regex can match the strings `ignorecase`, `igNoreCase`, and `IgnoreCase`.

For example, if you have freecodecamp, and you want to match it whether letters are uppercase or lowercase or both. Then here is the code:
```js
let myString = "freeCodeCamp";

let fccRegex = /freecodecamp/i; // Change this line

let result = fccRegex.test(myString);

console.log(result);
```
