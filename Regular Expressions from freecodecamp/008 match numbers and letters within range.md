You saw how you can use character sets to specify a group of characters to match, but that's a lot of typing when you need to match a large range of characters (for example, every letter in the alphabet). Fortunately, there is a built-in feature that makes this short and simple.
Inside a character set, you can define a range of characters to match using a hyphen character: `-`.
For example, to match lowercase letters `a` through `e` you would use `[a-e]`.
```js
let catStr = "cat";
let batStr = "bat";
let matStr = "mat";
let bgRegex = /[a-e]at/;
catStr.match(bgRegex);
batStr.match(bgRegex);
matStr.match(bgRegex);
```
In order, the three `match` calls would return the values `["cat"]`, `["bat"]`, and `null`.

Using the hyphen (`-`) to match a range of characters is not limited to letters. It also works to match a range of numbers.
For example, `/[0-5]/` matches any number between `0` and `5`, including the `0` and `5`.
Also, it is possible to combine a range of letters and numbers in a single character set.
```js
let jennyStr = "Jenny8675309";
let myRegex = /[a-z0-9]/ig;
jennyStr.match(myRegex);
```