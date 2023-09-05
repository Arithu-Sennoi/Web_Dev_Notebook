
### Function declaration
To make a function in JavaScript, one way is to use function declaration.
```js
function calcRectArea(width, height) {
return width * height;
}

console.log(calcRectArea(5, 6));
```
A `function` declaration creates a function object. Each time when a function is called, it returns the value specified by the last executed return statement, or undefined if the end of the function body is reached.

### Function expression
You can define a function inside an expression using function keyword, as follow:
```js
const getRectArea = function (width, height) {
return width * height;
};

console.log(getRectArea(3, 4));
```
Remember to put a semi colon at the end of function expression, since it is basically just an expression. 
`const thing = function(params){ //code;};`

In function expression, you do not have to name the function. You would just create a variable, and pass the function as the value of the variable. Functions without name are called `anonymous functions`. 

#### IIFE
function expressions can be used as an IIFE(Immediately Invoked Function Expression), which runs as soon as it is declared. 
Basically, a sort of function that runs immediately, right after it is defined.
To make an IIFE, create a function expression normally, but encapsulate the entire function expression inside "()" and then put another set of colons after them. Here is an example:
```js
const exampleFunction = (function() {
  console.log("This function runs immediately.");
})();

```
In this code, the function is defined inside parentheses and is followed by another set of parentheses `(function() { /* code */ })()`. The outer parentheses wrap the function expression, and the inner parentheses immediately call (invoke) the function.

### Difference b/n function declaration and function expression (from chatGPT)
Let's break down function declarations and function expressions in a beginner-friendly way:

**Function Declaration:**

1. **Definition:**
   A function declaration is a way to define a reusable block of code that can be called by its name. It's like giving a name to a set of instructions.

   ```javascript
   function sayHello() {
     console.log("Hello!");
   }
   ```

2. **Hoisting:**
   Function declarations are hoisted, which means they are moved to the top of their containing scope during the code execution. This allows you to call the function even before you define it in your code.

   ```javascript
   sayHello(); // This works because of hoisting

   function sayHello() {
     console.log("Hello!");
   }
   ```

3. **Scope:**
   Function declarations have a broader scope. They are accessible from anywhere within their containing function or script.

   ```javascript
   function sayHello() {
     console.log("Hello!");
   }

   sayHello(); // This works
   ```

**Function Expression:**

1. **Definition:**
   A function expression is a way to define a function as a value assigned to a variable. It's like storing a function in a box (variable).

   ```javascript
   const sayHello = function() {
     console.log("Hello!");
   };
   ```

2. **Hoisting:**
   Function expressions are not hoisted. You must define the variable and the function before you can use it.

   ```javascript
   sayHello(); // This would result in an error; not hoisted

   const sayHello = function() {
     console.log("Hello!");
   };
   ```

3. **Scope:**
   Function expressions are typically scoped to the variable they are assigned to. They are often used as anonymous functions (functions without a name) or as values of variables. This means they are more localized in scope.

   ```javascript
   const sayHello = function() {
     console.log("Hello!");
   };

   sayHello(); // This works because it's defined before use
   ```

**Choosing Between Them:**

- If you need a function that can be called before its declaration, or you want a function with a broader scope available throughout your code, use a function declaration.

- If you need a function as a value, want to control its scope, or use it locally in a specific context, use a function expression.

In practice, as a beginner, you'll often use function declarations for simpler cases and function expressions when you need more control over where and how the function is used. Over time, you'll become more comfortable with both approaches as you gain experience with JavaScript.

end of chatGPT response.

---
### Uses of function expression. 
Read the stuff above too. 

One of the main uses of creating an anonymous function is when you need a function that is only used once or as a callback function. 
```js
setTimeout(function() {
  console.log("This is an anonymous function.");
}, 1000);
```
above, we are passing an anonymous function as a param to setTimeout. 
setTimeout takes 2 params, it waits till time specified by 2nd param, and then executes function at first param. 
Normally, for thes, you would have to first define a function, then pass it as param to the function. But you can shorten the code, by passing that function directly as a param, which can only be done by function expression. 

Here is another example:
```js
const numbers = [1, 2, 3, 4, 5];
const squared = numbers.map(function(x) {
    return x * x;
});

```
refer to [[array.prototype.map()]] for more details. 
