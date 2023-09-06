Modules are a way to easily share code among JavaScript files. You can split JavaScript programs into multiple modules that can be imported when needed. 

JS modules use `import` and `export` statements. 

In order to use module functionality, you need to create a script in HTML document, with a type of module.
```html
<script type="module" scr="filename.js"></script>
```
This script can now import and export features. 

### Export
In javascript, if you have file with function that you want to use in other files, then you need to export it. 
```js
export const add = (x, y) => {
	return x+y;
}
```
In this code, before the add function is declared, we put export keyword. 
Above is a common way to export a single function, but you can achieve the same this like this:
```js
const add = (x, y) => {
	return x+y;
}

export {add};
```
If you have multiple functions that you want to export, you can use above way:
```js
export {add, sub, multiply, function1, function3};
```
Above code, exports 5 functions. 


### Import
In above code, we set 5 functions for export. Let that file name be "functions.js".
Now if you want to import 2 of those function in another file, 
```js
import { add, sub } from './math_functions.js';
```
./math_functions.js` is the relative path to that file, from current one. 

#### from freecodecamp
Suppose you have a file and you wish to import all of its contents into the current file. This can be done with the `import * as` syntax. Here's an example where the contents of a file named `math_functions.js` are imported into a file in the same directory:
```js
import * as myMathModule from "./math_functions.js";
```
The above `import` statement will create an object called `myMathModule`. This is just a variable name, you can name it anything. The object will contain all of the exports from `math_functions.js` in it, so you can access the functions like you would any other object property. Here's how you can use the `add` and `subtract` functions that were imported:
```js
myMathModule.add(2,3);
myMathModule.subtract(5,3);
```