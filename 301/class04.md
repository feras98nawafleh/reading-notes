# JavaScript — The Conditional (Ternary) Operator Explained
Starting With the Basics — The if statement
Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.
Consider the following example:
We have a person object that consists of a name, age, and driver property.
```
let person = {
  name: 'tony',
  age: 20,
  driver: null
};
```
We want to test if the age of our person is greater than or equal to 16. If this is true, they’re old enough to drive and driver should say 'Yes'. If this is not true, driver should be set to 'No'.
We could use an if statement to accomplish this:
```
if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}
```
But what if I told you we could do the same exact thing in just one line of code? Well, here it is:
```
person.driver = person.age >=16 ? 'Yes' : 'No';
```
```
condition ? value if true : value if false
```
Example — Driver Age
We’ll take a moment to revisit the initial example in this article:
```
let person = {
  name: 'tony',
  age: 20,
  driver: null
};
person.driver = person.age >=16 ? 'Yes' : 'No';
```
