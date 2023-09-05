#### from freecodecamp.org
In Javascript, an array can hold different datatypes. 
```js
let myArray = ["someName", 5, 12, 34.12, ["hola", 23]];
```
Ofcourse arrays can hold other arrays too. 

### array mutability
Unlike strings, entries of arrays are mutable. Means, they can change freely. 
Even if you declare your array with const, you can still change it's contents. But you cannot assign it to a new array. 
Below code works.
```js
const myArray = [1, 2, 3];

myArray.push(4); // This is allowed because it doesn't reassign `myArray`

console.log(myArray); // Output: [1, 2, 3, 4]

myArray[0] = 0; // You can modify individual elements

console.log(myArray); // Output: [0, 2, 3, 4]

```
But this one doesn't
```js
const myArray = [1, 2, 3];
myArray = [4, 2, 3]; // This will result in an error!!!
```
Because you are reassigning the array to a new array, instead of changing it. 


### push function
After declaring an array, you can even add more contents to it. One easy way to do that is using `push()` function. 
`.push()` takes one or more parameters and "pushes" them onto the end of the array.
```js
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```
`arr1` now has the value `[1, 2, 3, 4]` and `arr2` has the value 
`["Stimpson",  J", "cat", ["happy", "joy"]]`.

### pop function
`.pop()` is used to remove a value off the end of an array. It will remove it and will return it. 
```js
const myArray = [1,4,5];
const oneDown = myArray.pop();
console.log(myArray); //This will output: 1,4
console.log(oneDown); //This will output: 5
```
You can have arrays inside arrays and this would obviously work
```js
const myArray = [["hello", 1], ["this", 42], ["good", 99.99]];
console.log(myArray.pop()); // output: [ 'good', 99.99 ]
```
### shift function
Works just like `pop()` function, but it removes first item from the array.
```js
const ourArray = ["Stimpson", "J", ["cat"]];
console.log(ourArray.shift()); //output: ["J",["cat"]]
```
### unshift function
You can remove elements from start of the array. But what if you want to add stuff to the start of the array? 
`.unshift()` works exactly like `.push()`, but instead of adding the element at the end of the array, `unshift()` adds the element at the beginning of the array.
```js
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```
After the `shift`, `ourArray` would have the value `["J", "cat"]`. After the `unshift`, `ourArray` would have the value `["Happy", "J", "cat"]`.