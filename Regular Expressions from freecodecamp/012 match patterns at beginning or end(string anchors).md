If you have bunch of strings that start with different words, and you want to match all those strings with a regex pattern so that, only strings with specific stuff at the start should return true? 

In an earlier challenge, you used the caret character (`^`) inside a character set to create a negated character set in the form `[^thingsThatWillNotBeMatched]`. Outside of a character set, the caret is used to search for patterns at the beginning of strings.
```js
let firstString = "Ricky is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString);
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst);
```
The first `test` call would return `true`, while the second would return `false`.
So it will check if first part matches the pattern. 

There is also a method to match the last part of the string. 
You can search the end of strings using the dollar sign character `$` at the end of the regex.
```js
let theEnding = "This is a never ending story";
let storyRegex = /story$/;
storyRegex.test(theEnding);
let noEnding = "Sometimes a story will have to end";
storyRegex.test(noEnding);
```
The first `test` call would return `true`, while the second would return `false`.