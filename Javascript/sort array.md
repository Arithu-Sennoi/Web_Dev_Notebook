## For strings-
```js
let fruits = ["banana", "apple", "orange", "mango"]; 
fruits = fruits.sort(); 
//fruits = fruits.sort().reverse(); 
for(let fruit of fruits){ 
	console.log(fruit);
}
```
it would sort the array of strings in alphabetical order. 

## For numbers

```js
let grades = [100, 50, 90, 60, 80, 70];
grades = grades.sort(descendingSort);
grades.forEach(print);
function descendingSort(x, y){
	return y - x; 
} 
function ascendingSort(x, y){
	return x - y; 
} 
function print(element){
	console.log(element);
}
```

function(a, b){return a - b} When the sort() function compares two values, it sends the values to the compare function, and sorts the values according to the returned (negative, zero, positive) value. If the result is negative a is sorted before b. If the result is positive b is sorted before a. If the result is 0 no changes are done with the sort order of the two values.



### Syntax

_array_.sort(_compareFunction_)

### Parameters

|Parameter|Description|
|-----------|-------------|
|_compareFunction_|Optional.  <br>A function that defines a sort order. The function should return a negative, zero, or positive value, depending on the arguments:<br><br>- function(a, b){return a-b}<br><br>When sort() compares two values, it sends the values to the compare function, and sorts the values according to the returned (negative, zero, positive) value.<br><br>**Example:**<br><br>The sort function will sort 40 as a value lower than 100.<br><br>When comparing 40 and 100, sort() calls the function(40,100).<br><br>The function calculates 40-100, and returns -60 (a negative value).|

### More Examples

#### Sort numbers in ascending order:

const points = [40, 100, 1, 5, 25, 10];  
points.sort(function(a, b){return a-b});  

#### Sort numbers in descending order:

const points = [40, 100, 1, 5, 25, 10];  
points.sort(function(a, b){return b-a});  

#### Find the lowest value:

const points = [40, 100, 1, 5, 25, 10];  
  
// Sort the numbers in ascending order  
points.sort(function(a, b){return a-b});  
  
let lowest = points[0];

#### Find the highest value:

const points = [40, 100, 1, 5, 25, 10];  
  
// Sort the numbers in descending order:  
points.sort(function(a, b){return b-a});  
  
let highest = points[0];

#### Find the highest value:

const points = [40, 100, 1, 5, 25, 10];  
  
// Sort the numbers in ascending order:  
points.sort(function(a, b){return a-b});  
  
let highest = points[points.length-1];
