In Javascript, Strings are immutable, whichmeans that they cannot be altered once created.
For example, the following code will produce an error because the letter `B` in the string `Bob` cannot be changed to the letter `J`:

```js
let myStr = "Bob";
myStr[0] = "J";
```

Note that this does _not_ mean that `myStr` could not be re-assigned. The only way to change `myStr` would be to assign it with a new value, like this:

```js
let myStr = "Bob";
myStr = "Job";
```
