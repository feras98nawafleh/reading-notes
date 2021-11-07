# Python Scope & the LEGB Rule
## what is Scope?
it's the concept of how variables and functions can be found in the code, is it accessable or not?
there are 2 types of scope:
1. local scope: Can be used only in the scoped defined in
2. global scope: Can be used anywhere in the code

From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called __main__ to hold the main program’s execution. The namespace of this module is the main global scope of your program
Variables that are defined inside a function body have a local scope, and those defined outside have a global scope.

This means that local variables can be accessed only inside the function in which they are declared, whereas global variables can be accessed throughout the program body by all functions. When you call a function, the variables declared inside it are brought into scope.

## Example:
```python
#!/usr/bin/python
total = 0; # This is global variable.
# Function definition is here
def sum( arg1, arg2 ):
   # Add both the parameters and return them."
   total = arg1 + arg2; # Here total is local variable.
   print "Inside the function local total : ", total
   return total;
# Now you can call sum function
sum( 10, 20 );
print "Outside the function global total : ", total
```
## Output:
```python
Inside the function local total : 30
Outside the function global total : 0
```
### Create a nonlocal variable
```python
def outer():
    x = "local"

    def inner():
        nonlocal x
        x = "nonlocal"
        print("inner:", x)

    inner()
    print("outer:", x)


outer()
```
output:
```python
inner: nonlocal
outer: nonlocal
```
