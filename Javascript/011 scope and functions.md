#### from freecodecamp.org
In JavaScript, scope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code.
Variables which are declared without the `let` or `const` keywords are automatically created in the `global` scope. This can create unintended consequences elsewhere in your code or when running a function again. You should always declare your variables with `let` or `const`.

Variables which are declared within a function, as well as the function parameters, have local scope. That means they are only visible within that function.
Here is a function `myTest` with a local variable called `loc`.
```js
function myTest() {
  const loc = "foo";
  console.log(loc);
}

myTest();
console.log(loc);//will throw an error!!!
```
The `myTest()` function call will display the string `foo` in the console. The `console.log(loc)` line (outside of the `myTest` function) will throw an error, as `loc` is not defined outside of the function.


It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable.
In this example:
```js
const someVar = "Hat";

function myFun() {
  const someVar = "Head";
  return someVar;
}
```
The function `myFun` will return the string `Head` because the local version of the variable is present.