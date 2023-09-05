You can link to another page with the anchor (`a`) element. For example, `<a href='https://freecodecamp.org'></a>` would link to `freecodecamp.org`.

```<a href='www.arithusennoi.com'></a>``` would link to www.arithysennoi.com (which does not exist yet.)

But instead of displaying a link, to make it so that clicking a text would take you to the a link, you need to put text in between anchor tags. (between `<a> and </a>`.)

A link's text must be placed between the opening and closing tags of an anchor (`a`) element. For example, `<a href="https://www.freecodecamp.org">click here to go to freeCodeCamp.org</a>` is a link with the text `click here to go to freeCodeCamp.org`.

```<a href='www.arithusennoi.com'>click here to go to arithy sennoi web page.</a>```


you can also use anchor element to a text inside another element. for example,
```html
<p>this is a paragraph text. Click here to go to aruthu sennoi.</p>
```
here you can nest anchor element. 
```html
<p>this is a paragraph text. <a hrec='www.arithusennoi.com'>Click here to go to aruthu sennoi.</a></p>
```
adding a target attribute with element `_blank` to anchor element's opening tag `<a>` would make it so that the new wepage opened would open in a new tab. 
```html
<p>this is a paragraph text. <a hrec='www.arithusennoi.com' target='_blank'>Click here to go to aruthu sennoi.</a></p>
```
you can also use anchor element around images. it would make it so that clicking the image would open a link. 

```html
<a href='imageurlexample.com'><img src="imageurlexample.com" alt="example image"</a>
```
