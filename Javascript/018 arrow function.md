In JavaScript, we often don't need to name our functions, especially when passing a function as an argument to another function. Instead, we create inline functions. We don't need to name these functions because we do not reuse them anywhere else. We call such functions anonymous functions. 

To achieve this, we often use function expressions. 
```js
const myFunc = function() {
  const myVar = "value";
  return myVar;
}
```

ES6 provides us with the syntactic sugar to not have to write anonymous functions this way. Instead, you can use **arrow function syntax**:

```js
const myFunc = () => {
  const myVar = "value";
  return myVar;
}
```

When there is no function body, and only a return value, arrow function syntax allows you to omit the keyword `return` as well as the brackets surrounding the code. This helps simplify smaller functions into one-line statements:

```js
const myFunc = () => "value";
```

This code will still return the string `value` by default.

---
Arrow functions cannot be used as methods for objects. 
They also cannot be used as constructors for objects.

---
So, if there are no parameteres and the function just contains one return value, you can write the function like this:
```js
const myFunc = () => "some statement";
```
Above code, the function, returns the string "some statement". 

---
If there is only one param, and only 1 return statement in function body, you can write it like this:
```js
const myFunc = param1 => param1 * param1;
```
above code, takes 1 parameter called param1 and then returns this square. 

---
If there are multiple parameters, then you need to include brackets. 
```js
const myFunc = (param1, param2, param3) => param1 * param2 * param3;
```
above code takes 3 parameters and returns their product. 

---
if there are multiple lines of code inside the function body, then you need to include curly brackets and return statement for function body. 
```js
const myFunc = (param1, param2) => {
	console.log("performing myFunc function");
	return param1 * param2;
}
```

---
For arrow function, there are 2 types of bodies.
1. concise body
2. block body

Concise body is where you specify only a single expression, which is implicit return value. For example, `const func = (x) => x*x;`.

Block body is where you use curly braces to enclose a block of code. Inside it, you myst use an explicit return statement to specify what should be returned from the function. 


When you want to return an object using arrow function, you will have to take care, 
Returning object literals using the concise body syntax `(params) => { object: literal }` does not work as expected.
```js
const func = () => { foo: 1 };
// Calling func() returns undefined!

const func2 = () => { foo: function () {} };
// SyntaxError: function statement requires a name

const func3 = () => { foo() {} };
// SyntaxError: Unexpected token '{'
```
Above code does not work!!!


This is because JavaScript only sees the arrow function as having a concise body if the token following the arrow is not a left curly brace, so the code inside braces "{}" is parsed as a sequence of statements, where `foo` is a [label](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/label), not a key in an object literal.

To fix this, wrap the object literal in parentheses:
```js
const func = () => ({ foo: 1 });
```

