# CSS transition, transform

CSS transitions allows you to change property values smoothly, over a given duration.

Mouse over the element below to see a CSS transition effect:

CSS
In this chapter you will learn about the following properties:

transition
transition-delay
transition-duration
transition-property
transition-timing-function
Browser Support for Transitions

How to Use CSS Transitions?
To create a transition effect, you must specify two things:

the CSS property you want to add an effect to
the duration of the effect
Note: If the duration part is not specified, the transition will have no effect, because the default value is 0.

The following example shows a 100px * 100px red <div> element. The <div> element has also specified a transition effect for the width property, with a duration of 2 seconds:
example:
```css
div {
width: 100px;
height: 100px;
background: red;
transition: width 2s;
}
div:hover {
width: 300px;
}
div {
transition: width 2s, height 4s;
}
```
Specify the Speed Curve of the Transition
The transition-timing-function property specifies the speed curve of the transition effect.

The transition-timing-function property can have the following values:

ease - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
linear - specifies a transition effect with the same speed from start to end
ease-in - specifies a transition effect with a slow start
ease-out - specifies a transition effect with a slow end
ease-in-out - specifies a transition effect with a slow start and end
cubic-bezier(n,n,n,n) - lets you define your own values in a cubic-bezier function
Example:
```css
#div1 {transition-timing-function: linear;}
#div2 {transition-timing-function: ease;}
#div3 {transition-timing-function: ease-in;}
#div4 {transition-timing-function: ease-out;}
#div5 {transition-timing-function: ease-in-out;}
The following example shows some of the different speed curves that can be used:
```
# transform
CSS 2D Transforms Methods
With the CSS transform property you can use the following 2D transformation methods:

translate()
rotate()
scaleX()
scaleY()
scale()
skewX()
skewY()
skew()
matrix()
CSS 3D Transforms Methods
With the CSS transform property you can use the following 3D transformation methods:

rotateX()
rotateY()
rotateZ()
The rotateX() Method
Rotate X

The rotateX() method rotates an element around its X-axis at a given degree:

Example:
```css
#myDiv {
transform: rotateX(150deg);
}
```
The rotateY() Method
Rotate Y

The rotateY() method rotates an element around its Y-axis at a given degree:

Example:
```css
#myDiv {
transform: rotateY(150deg);
}
```
