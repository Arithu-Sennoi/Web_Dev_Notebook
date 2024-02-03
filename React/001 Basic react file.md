Note that this is not the right way to start a react project. This is just to get an understand of it. 
```html
<script crossorigin src="https://unpkg.com/react@17/umd/react.development.js"></script>

<script crossorigin src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>

<script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
```
Put above script tags in header section. 
Then connect your js file like this:
```html
<script type="text/babel" src="test.js"></script>
```
Alright, my first few minutes of learning react, this is my conclusion.

In normal programming languages, we make functions to reuse the same code again and again. And it also makes the main function look more simple. We can just put all functions in another file. This will simplify stuff.

Also, in C, we make custom, user declared functions and data types.
In this case, we make custom HTML elements. These elements are called componets. However, I do have some questions:

- In the tutorial, he showed code for a nav bar. It is huge, and instead of directly putting it in html, he made it into a react component. And added it as if it is a html element. But, you really won’t reuse a navbar like you would reuse a function. So it doesn’t make sense to make it into a component. 
