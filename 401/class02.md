# TDD with Python
TDD stands for test driven development, which is basically testing your code every minute, and the code itself is based on previous test the development team already made.
when the developer is writing code, he has nothing much of new things and features to think of, the rule is simple, write a code that to that and supposed to return that, any error or not sticking to the TDD rules, an error will be raised.

# if __name__ == “__main__”:
we see that piece of code a lot in python (.py) files, but what it's all about? and what does it do?
it has to do basically with the interpreter, since python is an interpreted language (not compiled), the interpreter which is responsible for translating the code to the machine (converting python code .py files into machine code),
Why Do we need it?
if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.
# Recursion
## what is recursion? what is functional programming?
it's basically the process of the function calling it self, as a first impression you'd think of infinite loop, but no, when using recursion there's always a base case when the function stops,
notice the following code example:
```
# A Python 3 program to
# demonstrate working of
# recursion


def printFun(test):

	if (test < 1):
		return
	else:

		print(test, end=" ")
		printFun(test-1) # statement 2
		print(test, end=" ")
		return

# Driver Code
test = 3
printFun(test)

# This code is contributed by
# Smitha Dinesh Semwal
```
