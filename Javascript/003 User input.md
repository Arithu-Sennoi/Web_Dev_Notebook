There is an easy way to get user input. That is via a window promt. 

```js
let username = window.prompt("what's your name?");
console.log(username);
```

The otherway is to use html textbox. 
Let there be an html element `<input>` with type=text, and id is myText.
and a button with id=sumbitBtn
```js
document.getElementById("submitBtn").onClick = function(){
	let username = document.getElementById("myText").value;
	console.log(username);
}
```
Now, when you write something in textbox, and click sumbit, it will take whatever text is in that textbox and assign it to variable username. 

Note that we didn't link input text box with the button. We just created a function that takes the value within the textbox and assigns it to a variable. And we call this function when ever user clicked the button. 