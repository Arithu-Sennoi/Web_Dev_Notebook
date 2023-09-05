Javascript is not a typed language. Meaning, you do not have to declare a datatype when you create a variable. So when you compare 2 different data types using equality operator, it converts one data type to other. 
```js
1   ==  1  // true
1   ==  2  // false
1   == '1' // true
"3" ==  3  // true
```
# strict equality
equality (`===`) is the counterpart to the equality operator (`==`). However, unlike the equality operator, which attempts to convert both values being compared to a common type, the strict equality operator does not perform a type conversion.

If the values being compared have different types, they are considered unequal, and the strict equality operator will return false.
**Examples**
```js
3 ===  3  // true
3 === '3' // false
```
In the second example, `3` is a `Number` type and `'3'` is a `String` type.

Note: in Javascript, you can determine the type of a variable using typeof operator, as follows
```js
console.log(typeof 3); //output: number
console.log(typeof '3'); //output: string
```
It works same way with variables. 


 Like the equality operator, the inequality operator will convert data types of values while comparing.
**Examples**
```js
1 !=  2    // true
1 != "1"   // false
1 != '1'   // false
1 != true  // false
0 != false // false
```
The strict inequality operator (`!==`) is the logical opposite of the strict equality operator. It means "Strictly Not Equal" and returns `false` where strict equality would return `true` and _vice versa_. The strict inequality operator will not convert data types.
**Examples**
```js
3 !==  3  // false
3 !== '3' // true
4 !==  3  // true
```
