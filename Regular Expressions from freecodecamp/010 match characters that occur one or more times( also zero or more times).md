Sometimes, you need to match a character (or group of characters) that appears one or more times in a row. This means it occurs at least once, and may be repeated.

You can use the `+` character to check if that is the case. Remember, the character or pattern has to be present consecutively. That is, the character has to repeat one after the other.

For example, `/a+/g` would find one match in `abc` and return `["a"]`. Because of the `+`, it would also find a single match in `aabc` and return `["aa"]`.

If it were instead checking the string `abab`, it would find two matches and return `["a", "a"]` because the `a` characters are not in a row - there is a `b` between them. Finally, since there is no `a` in the string `bcd`, it wouldn't find a match.
saying a+ here, is same as typing `a|aa|aaa|aaaa|...` till infinity. 

If you want to match charecters that occur zero or more times, you can use asterisk
```js
let soccerWord = "gooooooooal!";
let gPhrase = "gut feeling";
let oPhrase = "over the moon";
let goRegex = /go*/;
soccerWord.match(goRegex);
gPhrase.match(goRegex);
oPhrase.match(goRegex);
```
In order, the three `match` calls would return the values `["goooooooo"]`, `["g"]`, and `null`.
Here, the letter o, in go* has the asterisk. So it is same as saying:
`g|go|goo|gooo|goooo|....` to infinity.
If you had used plus charecter instead of asterisk, then it would be this:`go|goo|gooo|...` till infinity. Notice that the case `g` would not be matched for `+` charecter, but it does for `*`.

`/he.*lo/` here would mean, match words that have 'he' has first 2 letters, then there could be literllay anything(since there is a wildcard charecter), for any number of times(since there is a asterick), then it should end with 'lo'. 
For example,
"he this is just some random text lol lo" would match for our regex pattern. 
"hethisis onther 1233124 (*^&*^#$)lo" would also match for our pattern. 
"helo" would also match for our pattern. 
etc etc etc.
