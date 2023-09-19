In regular expressions, by default the match finds the longest part of string that fits the regex pattern and returns it. It is called greedy match. 
For example: 
```js
let text = "He said \"no more!\""
let myRegex = /".*"/ig;
let result = text.match(myRegex);
console.log(result);//output: "no more!"
```
Above code takes whatever the part with double quotes is, and returns it. But sometimes we do not want the longest possible part. 
```js
let regexp = /".+"/g; 
let str = 'a "witch" and her "broom" is one'; 
alert( str.match(regexp) ); //output: "witch" and her "broom"
```
Here, we only want "witch" and "broom", but not the full part. It returns that long part, because it is the longest string that fits our pattern. In such case, we could use lazy match. 

you can use the `?` character to change it to lazy matching. 
so `regexp = /".+?"/g;` would only return the shortest parts of the string that match the pattern. In above case, it would return both "witch" and "broom" in an array, since we used the `g` flag. 
