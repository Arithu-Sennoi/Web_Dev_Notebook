You can also match the whitespace or spaces between letters.
You can search for whitespace using `\s`, which is a lowercase `s`. This pattern not only matches whitespace, but also carriage return, tab, form feed, and new line characters. You can think of it as similar to the character class `[ \r\t\f\n\v]`
```js
let whiteSpace = "Whitespace. Whitespace everywhere!"
let spaceRegex = /\s/g;
whiteSpace.match(spaceRegex);
```
This `match` call would return `[" ", " "]`.

Subsequently, to search for everything except whitespace, you can use `\S` which is uppercase `s`. It is same as using `[^ \r\t\f\n\v]`. 
```js
let whiteSpace = "Whitespace. Whitespace everywhere!"
let nonSpaceRegex = /\S/g;
whiteSpace.match(nonSpaceRegex).length;
```
The value returned by the `.length` method would be `32`.