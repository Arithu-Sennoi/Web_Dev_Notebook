A pseudo-class is used to define a special state of an element.

For example, it can be used to:

- Style an element when a user mouses over it
- Style visited and unvisited links differently
- Style an element when it gets focus

The syntax of pseudo-classes:

```css
selector:pseudo-class { 
	property: value;
}
```


### anchor pseudo-classes.
Links can be displayed in different ways:

##### Example

```css

/* unvisited link */  
a:link {  color: #FF0000;}  
  
/* visited link */  
a:visited {  color: #00FF00;}  
  
/* mouse over link */  
a:hover {  color: #FF00FF;}  
  
/* selected link */  
a:active {  color: #0000FF;}
```

**Note:** `a:hover` MUST come after `a:link` and `a:visited` in the CSS definition in order to be effective! `a:active` MUST come after `a:hover` in the CSS definition in order to be effective! Pseudo-class names are not case-sensitive.

psuedo-classes can be combined with html classes. Say, we have a button with class="submit_button". we can set it, so that it will change color with we hover on it. 
```css
.submit_button:hover {
	background-color: #D3D3D3
}
```

