# Reading and Writing Files in Python
before anything, we know that any file is composed of three main parts:
1. Header
2. Data (body)
3. End of File (EOF)

**file path is the string that describes the file's location**
## just like anyother PL, python allows handling files
### opening a file in python
```python file = open('dog_breeds.txt') ```
Other options for modes:
'r'	Open for reading (default)
'w'	Open for writing, truncating (overwriting) the file first
'rb' or 'wb'	Open in binary mode (read/write using byte data)

```python 
>>> f = open('dog_breeds.txt')
>>> f.readlines()  # Returns a list object
```
### Iterating Over Each Line in the File
```python
>>> with open('dog_breeds.txt', 'r') as reader:
>>>     # Read and print the entire file line by line
>>>     line = reader.readline()
>>>     while line != '':  # The EOF char is an empty string
>>>         print(line, end='')
>>>         line = reader.readline()
```
# Python Exceptions
first of all let's understand what is exceptions and what's the difference with syntax errors:
syntax error is when writing a line that doesn't go with the rules of the language, example:
```python
>>> print 'hello'
# syntax error: missing ()
>>> print( 0 / 0 ))
  File "<stdin>", line 1
    print( 0 / 0 ))
                  ^
SyntaxError: invalid syntax
```
exceptions is runtime errors that occured but everything is written right, example:
```python
>>> print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero
```
## just like any other language, python allows dealing with and raising exceptions, example:
```python x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
```
## python also have try and catch block but with catch named except, example: 
```python
try:
    linux_interaction()
except AssertionError as error:
    print(error)
    print('The linux_interaction() function was not executed')
    # ========================================================
    try:
    with open('file.log') as file:
        read_data = file.read()
except:
    print('Could not open file.log')
 ```
 ***else statement can be used to execute program if there's no exception***
 ```python
 try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    print('Executing the else clause.')
```
***finally is used to cleanup as it's the last block of handling exception and the last to be executed***
```python
try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    try:
        with open('file.log') as file:
            read_data = file.read()
    except FileNotFoundError as fnf_error:
        print(fnf_error)
finally:
    print('Cleaning up, irrespective of any exceptions.')
```
 
