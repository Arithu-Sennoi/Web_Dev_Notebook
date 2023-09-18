Till now, we have only been checking if a string has given pattern or not, using `.test()` method. 
You can also extract the actual matches you found with `.match()` method.
To use the `.match()` method, apply the method on a string and pass in the regex inside the parentheses.
Here's an example:
```js
"Hello, World!".match(/Hello/);
let ourStr = "Regular expressions";
let ourRegex = /expressions/;
ourStr.match(ourRegex);
```
Here the first `match` would return `["Hello"]` and the second would return `["expressions"]`.

Note that the `.match` syntax is the "opposite" of the `.test` method you have been using thus far:
```js
'string'.match(/regex/);
/regex/.test('string');
```
It is a bit of a mess to remember. 
For text method, you pass the string in paras.
For match method, you pass the regex in paras.
