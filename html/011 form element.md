An HTML form is used to collect user input. The user input is most often sent to a server for processing.
The `<form>` element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.

A form element has action attribute.The `action` attribute defines the action to be performed when the form is submitted.
Usually, the form data is sent to a file on the server when the user clicks on the submit button.


The HTML `<input>` element is the most used form element.
An `<input>` element can be displayed in many ways, depending on the `type` attribute.

Here are some examples:

|Type|Description|
|---|---|
|``<input type="text">``|Displays a single-line text input field|
|``<input type="radio">``|Displays a radio button (for selecting one of many choices)|
|``<input type="checkbox">``|Displays a checkbox (for selecting zero or more of many choices)|
|``<input type="submit">``|Displays a submit button (for submitting the form)|
|``<input type="button">``|Displays a clickable button|

There are many kinds of inputs you can create using the `type` attribute. You can easily create a password field, reset button, or a control to let users select a file from their computer.

In order for a form's data to be accessed by the location specified in the `action` attribute, you must give the text field a `name` attribute and assign it a value to represent the data being submitted. For example, you could use the following syntax for an email address text field: `<input type="text" name="email">`. If the name attribute is ommited, then data of the form will not be sent. 

The input `placeholder` attribute specifies a short hint that describes the expected value of an input field (a sample value or a short description of the expected format).
The short hint is displayed in the input field before the user enters a value.
The `placeholder` attribute works with the following input types: text, search, url, tel, email, and password

To prevent a user from submitting your form when required information is missing, you need to add the `required` attribute to an `input` element. There's no need to set a value to the `required` attribute. Instead, just add the word `required` to the `input` element, making sure there is space between it and other attributes.

`label` elements are used to help associate the text for an `input` element with the `input` element itself (especially for assistive technologies like screen readers). For example, `<label><input type="radio"> cat</label>` makes it so clicking the word `cat` also selects the corresponding radio button.

When a button element is added inside a form element, it will have a default `type` attribute set to `submit`. 
When pressed by the user, it would submit the name and value attribute data to server.
example:
```html

<label><input id="indoor" type="radio" name="indoor-outdoor"> Indoor</label>
<label><input id="outdoor" type="radio" name="indoor-outdoor">Outdoor</label>
```
here after choosing either outdoor or indoor, and clicking the submit button, it will send to server the data, indoor-outdoor:on 
that is because it will only send name and value attributes, and we do not have value attribute. It is necessary to have same name attribute for radio buttons, so that only one can be choosen. then we will have to also give each button its own value attribute, so the data will have additional information on what has been selected. 

```html

<label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
<label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
```
here, if selected an option and submitted, it will have data sent will include the name attributes of those radio buttons, and will also have value attribute of which ever option choosen. 