# Forms and JS Events
## JS is very powerful and well knows as a connection between the user and the server, it sends data, do stuff as a response for a user's event made and all
JavaScript Form Validation
HTML form validation can be done by JavaScript.

If a form field (fname) is empty, this function alerts a message, and returns false, to prevent the form from being submitted:
```js
function validateForm() {
  let x = document.forms["myForm"]["fname"].value;
  if (x == "") {
    alert("Name must be filled out");
    return false;
  }
}
```
```html
<form name="myForm" action="/action_page.php" onsubmit="return validateForm()" method="post">
Name: <input type="text" name="fname">
<input type="submit" value="Submit">
</form>
```

HTML events are "things" that happen to HTML elements.

When JavaScript is used in HTML pages, JavaScript can "react" on these events.

HTML Events
An HTML event can be something the browser does, or something a user does.

Here are some examples of HTML events:

An HTML web page has finished loading
An HTML input field was changed
An HTML button was clicked
Often, when events happen, you may want to do something.

JavaScript lets you execute code when events are detected.

HTML allows event handler attributes, with JavaScript code, to be added to HTML elements.

With single quotes:
```html
<element event='some JavaScript'>
```
With double quotes:
```html
<element event="some JavaScript">
```
```js
<button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button>
```
Common HTML Events
Here is a list of some common HTML events:

Event and Description:
onchange =>	An HTML element has been changed
onclick	=> The user clicks an HTML element
onmouseover => The user moves the mouse over an HTML element
onmouseout => The user moves the mouse away from an HTML element
onkeydown	=> The user pushes a keyboard key
onload	=> The browser has finished loading the page
