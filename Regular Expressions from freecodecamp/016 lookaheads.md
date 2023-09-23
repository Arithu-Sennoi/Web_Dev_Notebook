Lookaheads are used to match patterns that does, or does not have a specific pattern immediately after it. 

There are 2 types of lookaheads: positive lookahead, negative lookahead. 

### Postive lookahead
A positive lookahead matches a specific pattern only if it is immediately followed by another specifed pattern. 
The syntax is `X(?=Y)`. Here `X` is our pattern that we are trying to match, and `Y` is the pattern that should be immediately after `X` for it to match. `X and Y` can be anything. A word, number, a complex pattern, etc.
```js
let quit = "qu";
let quRegex= /q(?=u)/;
quit.match(quRegex);
```
Here, it only matches with `q` in `quit` string, if it has `u` following it. 
`\d(?=px)` would match a digit (`\d`) only if it is immediately folled by `"px"`. So it would match 3 in `3px` but not 3 in `30px`. 

### Negative lookahead
A negative lookahead only matches a specific pattern if it is **not** immediately followed by another specified pattern. 
The syntax is  `X(?!Y)`. Where `X` is the pattern we want to match, and `Y` is the pattern that we want to make sure does not exist immediately after `X`.

For example, the regex `\d(?!px)` would match a digit (`\d`) only if it is NOT immediately followed by "px." So, it would match the "3" in "30px" but not the "3" in "3px."

Here is a more practical use of lookaheads. 
This is a (naively) simple password checker that looks for between 3 and 6 characters and at least one number:
```js
let password = "abc123";
let checkPass = /(?=\w{3,6})(?=\D*\d)/;
checkPass.test(password);
```