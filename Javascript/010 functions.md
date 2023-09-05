Here's an example of a function:
```js
function functionName() {
  console.log("Hello World");
}
```
You can call or invoke this function by using its name followed by parentheses, like this: `functionName();` 
Each time the function is called it will print out the message `Hello World` on the dev console. 
All of the code between the curly braces will be executed every time the function is called.

### paramenters and arguments
Parameters are variables that act as placeholders for the values that are to be input to a function when it is called. When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as arguments.

Here is a function with two parameters, `param1` and `param2`:
```js
function testFun(param1, param2) {
  console.log(param1, param2);
}
```
Then we can call `testFun` like this: `testFun("Hello", "World");`. We have passed two string arguments, `Hello` and `World`. Inside the function, `param1` will equal the string `Hello` and `param2` will equal the string `World`. Note that you could call `testFun` again with different arguments and the parameters would take on the value of the new arguments.

### Return a value
You can use return statement to send a value back out of the function.
```js
function plusThree(num) {
  return num + 3;
}

const answer = plusThree(5);
```

`answer` has the value `8`.

`plusThree` takes an argument for `num` and returns a value equal to `num + 3`.