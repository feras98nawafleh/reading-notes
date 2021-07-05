# HTML Lists, Control Flow with JS, and the CSS Box Model

## HTML lists:
HTML lists allow web developers to group a set of related items in lists.
An unordered HTML list:

Item
Item
Item
Item

An ordered HTML list:

1. First item
2. Second item
3. Third item
4. Fourth item

Unordered HTML List
An unordered list starts with the ul tag. Each list item starts with the li tag.
The list items will be marked with bullets (small black circles) by default:

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

Ordered HTML List
An ordered list starts with the ol tag. Each list item starts with the li tag.
The list items will be marked with numbers by default:

```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

## CSS box model

All HTML elements can be considered as boxes.
In CSS, the term "box model" is used when talking about design and layout.
The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.

Explanation of the different parts:

Content - The content of the box, where text and images appear
Padding - Clears an area around the content. The padding is transparent
Border - A border that goes around the padding and content
Margin - Clears an area outside the border. The margin is transparent
The box model allows us to add a border around elements, and to define space between elements.

```css
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```
## Control Flow with JS
JavaScript supports a compact set of statements, specifically control flow statements, that you can use to incorporate a great deal of
interactivity in your application. This chapter provides an overview of these statements.

The JavaScript reference contains exhaustive details about the statements in this chapter. The semicolon (;) character is used to separate statements in JavaScript code.

Any JavaScript expression is also a statement. See Expressions and operators for complete information about expressions.

Block statement
The most basic statement is a block statement, which is used to group statements. The block is delimited by a pair of curly brackets:

```js
{
  statement_1;
  statement_2;
  ⋮
  statement_n;
}
```
Example: 
Block statements are commonly used with control flow statements (if, for, while).

```js
while (x < 10) {
  x++;
}
// Here, { x++; } is the block statement.
```
