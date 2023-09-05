#### from freecodecamp.org
In order to help us create more flexible functions, ES6 introduces default parameters for functions.

```js
function greeting(name = "Anonymous"){
	return "hello" + name;
}
```

Check out this code:

```js
const greeting = (name = "Anonymous") => "Hello " + name;

console.log(greeting("shi"));
console.log(greeting());
```

The console will display the strings `Hello shi` and `Hello Anonymous`.

In above cases, if you call the function `greeting()` without any params, it assings defualt params and then execute the function. If you do give params, it will use them to excute then function instead. 