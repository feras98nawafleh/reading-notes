# more of HTML CSS and JS

*code snippet*
```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
and when we want to link the above html page with css file, for example style.css we use the <link> tag as follows:

```html
<link rel="stylesheet" href="style.css">
```

we can also write the css at the same html page with two ways:

1. inline

```html
<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>
```

2. internal

```html
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
```

## JavaScript for more dynamic page
JS is the language used in browsers to give life to the web page, it controls events, move things, redirect and handle server requests,
a very powerful language, open-sourced, free to learn and use, it's just amazing.

*code snippets*

```js
//many ways to define a variable
var name = ''
let name = ''
const name = ''
```

```js
if(condition) {
//do something
} else {
//do other thing
}

//chaining multiple if
if(condition) {
//do something
} else if {
//do other thing
} else if(condition) {
//do something
} else if{
//do other thing
}
```

```js
while(condition){
//keep do something
}

for(var i=0;i<5;i++) {
//do something 5 times
}

```

# Git commit -m "WHY!!!!!"
*when commiting a change to the repo, it's always the best practise to add a description of why you did that change*
Why good commit messages matter? If you browse the log of any random Git repository, you will probably find its commit messages are more or less a mess.

## The seven rules of a great Git commit message
Keep in mind: This has all been said before.
1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

