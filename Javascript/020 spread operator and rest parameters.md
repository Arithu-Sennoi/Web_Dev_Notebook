### spread operator
```js
// spread operator = allows an iterable such as an 
// ... array or string to be expanded 
// in places where zero or more 
// arguments are expected 
// (unpacks the elements) 
let class1 = ["Spongebob", "Patrick", "Sandy"];
let class2 = ["Squidward", "Mr.Krabs", "Plankton"];
class1.push(...class2);
console.log(...class1);


let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let maximum = Math.max(...numbers);
console.log(maximum);
/*  */
```

In the first part of the code, we want to push all of class2 into class1. But if we do: 
`class1.push(class2)` it wont push the items in class2 to class1. Instead, it pushes an array as an object into class1. 
We could use spread operator here, and it would take the contents of the class2 and seperate them. so, writing `class1.push(...class2);` is same as writing: 
`class1.push("Squidward", "Mr.Krabs", "Plankton");`
because it expanded the array. 

In the second part of the code, we have an array of integers, and we want the maximum. We cant use Math.max() directly on it, because that function expects arguments of integers, and we can't pass in an array. Here we could use spread operator. 

So basically, spread operators takes an arrays and other expressions and expands them. 
However, the spread operator only works in-place, like in an argument to a function or in an array literal. For example:
```js
const spreaded = [...arr];
```
However, the following code will not work:
```js
const spreaded = ...arr;
```
### rest paraments
Lets suppose, we have a sum function that adds given arguments.
If we make such that function takes 2 aruguments and returns their sum, then it wont work if we want sum of 3 numbers. But we do not want to create a seperate function for 3 arguements, 4 arguments, etc. 

When we use `...` operator and a name as an argument, Then all the user supplied parameters will be taken into an array of given name, and function uses that array. So we could have variable amount arguments. 
```js
// rest parameters = represents an indefinite number 
// ... of parameters 
// (packs arguments into an array) let a = 1; let b = 2;
let c = 3; let d = 4; let e = 5;
console.log(sum(a, b, c, d, e));
function sum(...numbers){ 
	let total = 0; 
	for(let number of numbers){ 
		total += number 
	} 
	return total 
}

```

---
# from MDN 
The **rest parameter** syntax allows a function to accept an indefinite number of arguments as an array, providing a way to represent [variadic functions](https://en.wikipedia.org/wiki/Variadic_function) in JavaScript.



```js
function sum(...theArgs) {
  let total = 0;
  for (const arg of theArgs) {
    total += arg;
  }
  return total;
}

console.log(sum(1, 2, 3));
// Expected output: 6

console.log(sum(1, 2, 3, 4));
// Expected output: 10

```

## syntax
```
function f(a, b, ...theArgs) {
  // …
}
```

## Description

A function definition's last parameter can be prefixed with `...` (three U+002E FULL STOP characters), which will cause all remaining (user supplied) parameters to be placed within an [`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) object.


```
function myFun(a, b, ...manyMoreArgs) {
  console.log("a", a);
  console.log("b", b);
  console.log("manyMoreArgs", manyMoreArgs);
}

myFun("one", "two", "three", "four", "five", "six");

// Console Output:
// a, one
// b, two
// manyMoreArgs, ["three", "four", "five", "six"]
```

A function definition can only have one rest parameter, and the rest parameter must be the last parameter in the function definition.


```
function wrong1(...one, ...wrong) {}
function wrong2(...wrong, arg2, arg3) {}
```

The rest parameter is not counted towards the function's [`length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/length) property.

### [The difference between rest parameters and the arguments object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters#the_difference_between_rest_parameters_and_the_arguments_object)

There are three main differences between rest parameters and the [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments) object:

- The `arguments` object is **not a real array**, while rest parameters are [`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) instances, meaning methods like [`sort()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort), [`map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map), [`forEach()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) or [`pop()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop) can be applied on it directly.
- The `arguments` object has the additional (deprecated) [`callee`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments/callee) property.
- In a non-strict function with simple parameters, the `arguments` object [syncs its indices with the values of parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments#assigning_to_indices). The rest parameter array never updates its value when the named parameters are re-assigned.
- The rest parameter bundles all the _extra_ parameters into a single array, but does not contain any named argument defined _before_ the `...restParam`. The `arguments` object contains all of the parameters — including the parameters in the `...restParam` array — bundled into one array-like object.

## [Examples](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters#examples)

### [Using rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters#using_rest_parameters)

In this example, the first argument is mapped to `a` and the second to `b`, so these named arguments are used as normal.

However, the third argument, `manyMoreArgs`, will be an array that contains the third, fourth, fifth, sixth, …, nth — as many arguments as the user specifies.

JSCopy to Clipboard

```
function myFun(a, b, ...manyMoreArgs) {
  console.log("a", a);
  console.log("b", b);
  console.log("manyMoreArgs", manyMoreArgs);
}

myFun("one", "two", "three", "four", "five", "six");

// a, "one"
// b, "two"
// manyMoreArgs, ["three", "four", "five", "six"] <-- an array
```

Below, even though there is just one value, the last argument still gets put into an array.

JSCopy to Clipboard

```
// Using the same function definition from example above

myFun("one", "two", "three");

// a, "one"
// b, "two"
// manyMoreArgs, ["three"] <-- an array with just one value
```

Below, the third argument isn't provided, but `manyMoreArgs` is still an array (albeit an empty one).

```
// Using the same function definition from example above

myFun("one", "two");

// a, "one"
// b, "two"
// manyMoreArgs, [] <-- still an array
```

Below, only one argument is provided, so `b` gets the default value `undefined`, but `manyMoreArgs` is still an empty array.

```
// Using the same function definition from example above

myFun("one");

// a, "one"
// b, undefined
// manyMoreArgs, [] <-- still an array
```

### [Argument length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters#argument_length)

Since `theArgs` is an array, a count of its elements is given by the [`length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length) property. If the function's only parameter is a rest parameter, `restParams.length` will be equal to [`arguments.length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments/length).

```
function fun1(...theArgs) {
  console.log(theArgs.length);
}

fun1(); // 0
fun1(5); // 1
fun1(5, 6, 7); // 3
```

### [Using rest parameters in combination with ordinary parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters#using_rest_parameters_in_combination_with_ordinary_parameters)

In the next example, a rest parameter is used to collect all parameters after the first parameter into an array. Each one of the parameter values collected into the array is then multiplied by the first parameter, and the array is returned:

```
function multiply(multiplier, ...theArgs) {
  return theArgs.map((element) => multiplier * element);
}

const arr = multiply(2, 15, 25, 42);
console.log(arr); // [30, 50, 84]
```

### [From arguments to an array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters#from_arguments_to_an_array)

[`Array`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) methods can be used on rest parameters, but not on the `arguments` object:

```
function sortRestArgs(...theArgs) {
  const sortedArgs = theArgs.sort();
  return sortedArgs;
}

console.log(sortRestArgs(5, 3, 7, 1)); // 1, 3, 5, 7

function sortArguments() {
  const sortedArgs = arguments.sort();
  return sortedArgs; // this will never happen
}

console.log(sortArguments(5, 3, 7, 1));
// throws a TypeError (arguments.sort is not a function)
```

Rest parameters were introduced to reduce the boilerplate code that was commonly used for converting a set of arguments to an array.

Before rest parameters, `arguments` need to be converted to a normal array before calling array methods on them:

```
function fn(a, b) {
  const normalArray = Array.prototype.slice.call(arguments);
  // — or —
  const normalArray2 = [].slice.call(arguments);
  // — or —
  const normalArrayFrom = Array.from(arguments);

  const first = normalArray.shift(); // OK, gives the first argument
  const firstBad = arguments.shift(); // ERROR (arguments is not a normal array)
}
```

Now, you can easily gain access to a normal array using a rest parameter:

```
function fn(...args) {
  const normalArray = args;
  const first = normalArray.shift(); // OK, gives the first argument
}
```