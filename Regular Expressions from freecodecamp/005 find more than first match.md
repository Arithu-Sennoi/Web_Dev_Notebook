So far our pattern matching only searches and matches for the word once. 
To search or extract a pattern more than once, you can use the global search flag: `g`. it would return all parts of the string that match our pattern in an array. 
```js
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);
```
And here `match` returns the value `["Repeat", "Repeat", "Repeat"]`.
