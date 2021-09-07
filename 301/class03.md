# Passing Functions as Props
## Lists and Keys
```
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled);
```
This code logs [2, 4, 6, 8, 10] to the console.

In React, transforming arrays into lists of elements is nearly identical.

Rendering Multiple Components
You can build collections of elements and include them in JSX using curly braces {}.

Below, we loop through the numbers array using the JavaScript map() function. We return a <li> element for each item. Finally, we assign the resulting array of elements to listItems:
```
  const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
);
```
We include the entire listItems array inside a <ul> element, and render it to the DOM:
```
ReactDOM.render(
  <ul>{listItems}</ul>,
  document.getElementById('root')
);
```
```
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li>{number}</li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```
## How to Use the Spread Operator (…) in JavaScript
The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.
What is ... used for?
“Spread operator to the rescue! It looks similar to rest parameters, also using ..., but does quite the opposite.” — JavaScript.info
```
Math.max(1,3,5) // 5
Math.max([1,3,5]) // NaN
```
Trying to pass an array to a JavaScript function expecting separate arguments does not work. In this case it produces a NaN result. Enter …:
```
Math.max(...[1,3,5]) // 5
```
What else can … do?
The … spread operator is useful for many different routine tasks in JavaScript, including the following:
Copying an array
Concatenating or combining arrays
Using Math functions
Using an array as arguments
Adding an item to a list
Adding to state in React
Combining objects
Converting NodeList to an array
In each case, the spread syntax expands an iterable object, usually an array, though it can be used on any interable, including a string.
