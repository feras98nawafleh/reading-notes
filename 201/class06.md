# Problem Domain, Objects, and the DOM

## problem domain
Understanding the problem domain is the hardest part of programming.
Programming is easy if you understand the problem domain.
It is very difficult to solve a problem before you know the question. It’s like buzzing in on Jeopardy before you hear the clue and shouting out random questions.
You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.

## JS Objects
it's quite one of the most important things in programming as a whole and javascript in particular.
Objects are variables too. But objects can contain many values.
This code assigns many values (Fiat, 500, white) to a variable named car:
```js
const car = {type:"Fiat", model:"500", color:"white"};
```
The values are written as name:value pairs (name and value separated by a colon).

It is a common practice to declare objects with the const keyword.
```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

## The DOM
DOM stands for document object model
The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.

```js
const paragraphs = document.querySelectorAll("p");
// paragraphs[0] is the first <p> element
// paragraphs[1] is the second <p> element, etc.
alert(paragraphs[0].nodeName);
```

```js
<html>
  <head>
    <script>
       // run this function when the document is loaded
       window.onload = function() {

         // create a couple of elements in an otherwise empty HTML page
         const heading = document.createElement("h1");
         const heading_text = document.createTextNode("Big Head!");
         heading.appendChild(heading_text);
         document.body.appendChild(heading);
      }
    </script>
  </head>
  <body>
  </body>
</html>
```
