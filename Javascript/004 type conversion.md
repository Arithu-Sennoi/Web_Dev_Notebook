when we accept some user input in javascript, it will be stored as a string. 
but if we are expecting an interger, it could mess things up. 
```js
let age = window.prompt("how old are you?");
age = age + 1;
console.log("you will be ", age, " years old soon!");
//that will print: you will be 211 years old soon!
```
that is because when you initialize a varible in js, you dont specify it's type. Js will automatically assign it by itself. So it would assign user input to age and make a string type. 

You could assign "age" variable some interger value, and then assign it user input, it could work. 
but there are also other cases where you would want to change data type. This is how you do it. 
```js 
let age = window.prompt("how old are you?");
age = Number(age);
age = age + 1;
console.log("you will be ", age, " years old soon!");
//that will print: you will be 22 years old soon!
```
Note: make sure use capital 'N' for Number. 

`console.log(typeof age);` would print what datatype age is, to your console. 

to convert a number to a string: 
```js
let x = 3.14;
let y = string(x);
console.log(y, typeof y);//output:3.14 string
```
we mentioned that `splice()` can take up to three parameters? Well, you can use the third parameter, comprised of one or more element(s), to add to the array. This can be incredibly useful for quickly switching out an element, or a set of elements, for another.

```js
const numbers = [10, 11, 12, 12, 15];
const startIndex = 3;
const amountToDelete = 1;

numbers.splice(startIndex, amountToDelete, 13, 14);
console.log(numbers);
```

The second occurrence of `12` is removed, and we add `13` and `14` at the same index. The `numbers` array would now be `[ 10, 11, 12, 13, 14, 15 ]`.

Here, we begin with an array of numbers. Then, we pass the following to `splice()`: The index at which to begin deleting elements (3), the number of elements to be deleted (1), and the remaining arguments (13, 14) will be inserted starting at that same index. Note that there can be any number of elements (separated by commas) following `amountToDelete`, each of which gets inserted.

