```javascript
document.body.innerHTML = 'hello';
```
doing this, makes the entire webpage to only hello. 
`document.body` is the body element in html. `document.body.innerhtml` is the html code inside the body element. We set it equal to "hello", and hence the page will become blank with just the text hello. 

```javascript
document.getElementById("text").innerHTML="Try again.";
```
This code, will set the innerHTML of an element with id=text, to be "try again.".
You can display text, change text, etc in a webpage using this method. 

to trigger js code when clicked on a button, use this. 
```js
let count = 0;
document.getElementById("add").onclick = function(){
    count++;
}
```
here, we have a variable called count. We then refer it using it's Id and say, onclick do this function. 

One way to get input from user, is to use `<input>` elements. We can get them by id using javascript, and we can get the value inside them like this:
```javascript
ID = document.getElementById("myId").value;
```
this will assign the value inside input element with id='myId' to a variable called ID. 
so, you can have an input field, and when user clicks submit button, you can run above code. 


Here is an example of counter program:
```js
let count = 0;
document.getElementById("add").onclick = function(){
    count++;
    document.getElementById('text').innerHTML = count;
}

document.getElementById("sub").onclick = function(){
    count--;
    document.getElementById('text').innerHTML = count;
}

document.getElementById("reset").onclick = function(){
    count = 0;
    document.getElementById('text').innerHTML = count;
}
```
