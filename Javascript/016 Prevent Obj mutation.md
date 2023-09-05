#### from freecodecamp.org
Even if one declared an array or and object with const key word, they can still alter it. They just cannot assign the object to a new one. 
But if you want to make sure your data doesn't change, JavaScript provides a function `Object.freeze` to prevent data mutation. 

Any attempt at changing the object will be rejected, with an error thrown if the script is running in strict mode.
```js
let obj = {
  name:"FreeCodeCamp",
  review:"Awesome"
};
Object.freeze(obj);
obj.review = "bad";
obj.newProp = "Test";
console.log(obj); 
```
The `obj.review` and `obj.newProp` assignments will result in errors, because our editor runs in strict mode by default, and the console will display the value `{ name: "FreeCodeCamp", review: "Awesome" }`.