# Python Classes and Objects
## just like anyother programming language, python supports the OOP (object oriented programming), by allowing the developer to write new Class, he's like basically making new type to use.
Objects are an like variables ot functions into one entity. classes give variables and functions to their objects.
```python
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myObject = MyClass()
# myObject now have variable and function
```
objects have the power to access both variables and functions in their parent class by using the . operator, example regarding the previous code:
```python
myObject.function()
# This is a message inside the class.
print(myObject.variable)
# blah
```

# Recursion in Python (Thinking Recursively)
## Recursion means "defining a problem in terms of itself". This can be a very powerful tool in writing algorithms. Recursion comes directly from Mathematics, where there are many examples of expressions written in terms of themselves. For example, the Fibonacci sequence is defined as: F(i) = F(i-1) + F(i-2)

For example, we can define the operation "find your way home" as:

If you are at home, stop moving.

Take one step toward home.

"find your way home".

best examples to learn recursion in any programming language is the Factorial:
```python def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
```
