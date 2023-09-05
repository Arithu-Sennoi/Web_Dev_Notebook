`document.getElementById("myCheckbox").checked` will return true if the checkbox of input element with id="myCheckbox" is checked. 

```js
document.getElementById("myButton").onclick = function(){ 
	const myCheckBox = document.getElementById("myCheckBox"); 
	if(document.getElementById("myCheckBox").checked){ 
		console.log("You are subscribed!"); 
	} 
	else{ 
	console.log("You are NOT subscribed!"); 
	} 
}

```
