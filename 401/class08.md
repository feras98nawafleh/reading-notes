# List Comprehensions in Python
almost all python programs have lists, and there are a lot of operation we can apply to these lists like loops and so on.
python provides a thing called list comprehensions, a method to deal with lists in pyhton, List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.
## Notes about List Comprehensions:
1. it's more elegant and nicer way to manage lists and create new ones
2. creating lists in python using list comprehensions is more compact way. 
3. ist comprehension is faster than other list methods and more flexible than loops.

**Example 1: Creating a list with list comprehensions**
```python
# construct a basic list using range() and list comprehensions
# syntax
# [ expression for item in list ]
digits = [x for x in range(10)]

print(digits)
# output: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```
**Example 2: Comparing list creation methods in Python**
a quick comparison between loops and list comprehensions:
***Using Loops:***
```python
# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)
# output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```
***Using comprehensions:***
```python
# create a list using list comprehension
squares = [x**2 for x in range(10)]

print(squares)
# output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```
**Example 3: Using list comprehensions with strings**
```python
# a list of the names of popular authors
authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]

# create an acronym from the first letter of the author's names
letters = [ name[0] for name in authors ]
print(letters)
# output: ['E', 'L', 'F', 'T', 'E', 'S']
```
