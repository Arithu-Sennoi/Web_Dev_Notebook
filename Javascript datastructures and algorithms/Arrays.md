### Push() and unshift() methods.
Arrays have `.push()` and `.unshift()` methods to add elements.

- `.push()` adds the content inside the brackets to the array at the end.
- `.unshift()` adds the content inside the brackets to the array at the start.

You can also pass variables inside these methods. Note that these are variables, not objects. If you pass a variable that holds an integer value, it will add that value to the array. It won't add the variable itself to the array. However, if you push an object to the array, it will add that object as an element to the array.

Also, both these methods can take multiple values and add them to the array at the same time. 

```js
let twentyThree = 'XXIII';
let romanNumerals = ['XXI', 'XXII'];

romanNumerals.unshift('XIX', 'XX');
romanNumerals.push(twentyThree);

```
### pop() and shift() methods.
Now, `pop()` and `shift()` are opposite of `push()` and `unshift()`. `pop()` function removes the last element of the array. 
`shift()` function removes the first element of the array. 

Another things to note is that `pop()` and `shift()` methods do not take any arguments. **They also return the element they deleted.**
```js
function popShift(arr) {
let popped = arr.pop();
let shifted = arr.shift();
return [shifted, popped];
}

console.log(popShift(['challenge', 'is', 'not', 'complete']));
```
Above function takes an array as input, and returns a new array that that first and last values in it. You can see that pop() and shift() function return values that get assigned to popped and shifted variables. 
it can be shortened like this:
```js
function popShift(arr) {
return [arr.shift(), arr.pop()];
}

console.log(popShift(['challenge', 'is', 'not', 'complete']));
```
Here, we directly return the values given out by `shift()` and `pop()` methods, without creating a new variable. This explains that pop and shift actually return values. 

### splice() method.
So far, we learned how to remove elements from beginning and end of arrays. But what if we want to remove element from somewhere in the middle? Or remove more then one element at once? 
Well, that is where `spice()` comes in. It allows us to **remove any number of consective elements** from anywhere in an array. 

`splice()` can take up to 3 parameters, but for now, we'll focus on just the first 2. The first two parameters of `splice()` are integers which represent indexes, or positions, of items in the array that `splice()` is being called upon. And remember, arrays are _zero-indexed_, so to indicate the first element of an array, we would use `0`. `splice()`'s first parameter represents the index on the array from which to begin removing elements, while the second parameter indicates the number of elements to delete. For example:

```js
let array = ['today', 'was', 'not', 'so', 'great'];

array.splice(2, 2);
```

Here we remove 2 elements, beginning with the third element (at index 2). `array` would have the value `['today', 'was', 'great']`.

`splice()` not only modifies the array it's being called on, but it also returns a new array containing the value of the removed elements:

```js
let array = ['I', 'am', 'feeling', 'really', 'happy'];

let newArray = array.splice(3, 2);
```

`newArray` has the value `['really', 'happy']`.
### slice() method.
The next method we will cover is `slice()`. Rather than modifying an array, `slice()` copies or _extracts_ a given number of elements to a new array, leaving the array it is called upon untouched. `slice()` takes only 2 parameters — the first is the index at which to begin extraction, and the second is the index at which to stop extraction (extraction will occur up to, but not including the element at this index). Consider this:

```js
let weatherConditions = ['rain', 'snow', 'sleet', 'hail', 'clear'];

let todaysWeather = weatherConditions.slice(1, 3);
```

`todaysWeather` would have the value `['snow', 'sleet']`, while `weatherConditions` would still have `['rain', 'snow', 'sleet', 'hail', 'clear']`.

In effect, we have created a new array by extracting elements from an existing array.
### spread operator.
While `slice()` allows us to be selective about what elements of an array to copy, among several other useful tasks, ES6's new spread operator allows us to easily copy _all_ of an array's elements, in order, with a simple and highly readable syntax. The spread syntax simply looks like this: `...`

In practice, we can use the spread operator to copy an array like so:

```js
let thisArray = [true, true, undefined, false, null];
let thatArray = [...thisArray];
```

`thatArray` equals `[true, true, undefined, false, null]`. `thisArray` remains unchanged and `thatArray` contains the same elements as `thisArray`.

If you didn't use the spread operator for this operation, then you would be appending an array(`thisArray`) inside `thatArray`. So you would create a 2d array. But that is not what we wanted. To copy the elements of one array to another, in plain c language, we would use a loop to iterate over the array and add each element to this new array on every loop. But spread operator makes this easier. 

spread operator can also be used in middle of another array. see example:
```js
let thisArray = ['sage', 'rosemary', 'parsley', 'thyme'];

let thatArray = ['basil', 'cilantro', ...thisArray, 'coriander'];
```
`thatArray` would have the value `['basil', 'cilantro', 'sage', 'rosemary', 'parsley', 'thyme', 'coriander']`.

### .indexOf() method
You can find the index of any item in an array with this method. It returns the index. If the item you are searching for is not found, then it returns -1 as the index. 
```js
let myArr = ['apple', 'banana', 'orange', 'kiwi'];
return myArr.indexOf(kiwi); //returns '3' 
//because that is the index of kiwi in our array. 
```

