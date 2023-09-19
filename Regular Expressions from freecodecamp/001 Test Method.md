Regular expressions are used in programming languages to match parts of strings. You create patterns to help you do that matching.

If you want to find the word `the` in the string `The dog chased the cat`, you could use the following regular expression: `/the/`. Notice that quote marks are not required within the regular expression.

JavaScript has multiple ways to use regexes. One way to test a regex is using the `.test()` method. The `.test()` method takes the regex, applies it to a string (which is placed inside the parentheses), and returns `true` or `false` if your pattern finds something or not.

```js
let testStr = "freeCodeCamp";
let testRegex = /Code/;
testRegex.test(testStr);
```

The `test` method here returns `true`.

you searched for the word `Hello` using the regular expression `/Hello/`. That regex searched for a literal match of the string `Hello`. Here's another example searching for a literal match of the string `Kevin`:
```js
let testStr = "Hello, my name is Kevin.";
let testRegex = /Kevin/;
testRegex.test(testStr);
```
This `test` call will return `true`.
Any other forms of `Kevin` will not match. For example, the regex `/Kevin/` will not match `kevin` or `KEVIN`.
```js
let wrongRegex = /kevin/;
wrongRegex.test(testStr);
```
This `test` call will return `false`.

We will soon see how to match other forms as well. 