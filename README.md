Programming & Problem Solving  (PPS)
Unit III  |  Functions & Strings
Functions in Python
R. H. Sapat College of Engineering, Nashik
First Year Engineering  |  Academic Year 2025–26
 
Prepared by:  Mr. K. V. Deshmukh
Faculty, Dept. of MCA (Engineering)

 
 
Table of Contents
Table of Contents.......................................................................................................... 1
1.  Need for Functions.................................................................................................. 1
1.1  Why Do We Need Functions?........................................................................... 1
1.2  What is a Function?........................................................................................... 1
1.3  Advantages of Functions................................................................................... 1
2.  Defining and Calling a Function............................................................................ 1
2.1  How to Define a Function................................................................................. 1
2.2  Parameters vs. Arguments................................................................................ 1
2.3  Calling a Function.............................................................................................. 1
2.4  Your First Function — Step by Step................................................................. 1
3.  Indentation in Python............................................................................................. 1
4.  Scope and Lifetime of Variables............................................................................. 1
4.1  What is Scope?................................................................................................... 1
4.2  Local Variables................................................................................................... 1
4.3  Global Variables................................................................................................. 1
4.4  The global Keyword.......................................................................................... 1
4.5  Difference between Local and Global Variables............................................. 1
5.  The return Statement............................................................................................... 1
5.1  What is the return Statement?........................................................................... 1
5.2  Returning Multiple Values................................................................................ 1
5.3  Difference between return and print................................................................ 1
6.  Types of Functions.................................................................................................. 1
6.1  Built-in Functions............................................................................................... 1
6.2  User-Defined Functions..................................................................................... 1
Type 1 — No Parameter, No Return Value........................................................ 1
Type 2 — With Parameter, No Return Value..................................................... 1
Type 3 — No Parameter, With Return Value..................................................... 1
Type 4 — With Parameter, With Return Value (Most Common)..................... 1
7.  Default Arguments and Keyword Arguments..................................................... 1
7.1  Default Arguments............................................................................................ 1
7.2  Keyword Arguments......................................................................................... 1
8.  Lambda (Anonymous) Functions.......................................................................... 1
8.1  What is a Lambda Function?............................................................................ 1
8.2  Lambda vs Regular Function............................................................................ 1
8.3  Lambda with map()........................................................................................... 1
8.4  Lambda with filter()........................................................................................... 1
9.  Documentation Strings (Docstrings)...................................................................... 1
9.1  Single-Line Docstring........................................................................................ 1
9.2  Multi-Line Docstring......................................................................................... 1
10.  Good Programming Practices Using Functions.................................................. 1
Practice 1 — Use Meaningful Names...................................................................... 1
Practice 2 — One Function = One Task................................................................... 1
Practice 3 — Always Write a Docstring.................................................................. 1
Practice 4 — Use return Instead of Global Variables............................................. 1
Practice 5 — Keep Functions Short......................................................................... 1
Practice 6 — Test Your Function with Multiple Inputs......................................... 1
11.  Simple Programs Using Functions....................................................................... 1
Program 1 — Addition of Two Numbers............................................................... 1
Program 2 — Square of a Number.......................................................................... 1
Program 3 — Swap Two Numbers......................................................................... 1
Program 4 — Find Maximum of Three Numbers.................................................. 1
Program 5 — Check Even or Odd........................................................................... 1
Program 6 — Factorial of a Number....................................................................... 1
Program 7 — Check Prime Number....................................................................... 1
Program 8 — Reverse a String................................................................................. 1
Program 9 — Check Palindrome (String)............................................................... 1
Program 10 — Count Vowels in a String................................................................ 1
Program 11 — Simple Interest using Function...................................................... 1
Program 12 — Armstrong Number Check............................................................. 1
12.  Practice Problems................................................................................................... 1
Write the Following Programs Using Functions.................................................... 1
13.  Viva Voce and Exam Questions........................................................................... 1
14.  Quick Revision Summary..................................................................................... 1
 

 






1.  Need for Functions

1.1  Why Do We Need Functions?
Imagine you are writing a program that calculates the area of a circle at five different places. Without functions, you would have to write the same formula — area = 3.14 * r * r — five separate times. If you later discover a mistake in that formula, you must find and fix it in five places. This is error-prone, time-consuming, and makes your code look messy. Functions solve this problem completely.
 
The core problems that functions solve are:
•     Code repetition: The same logic has to be written again and again at multiple places in the program.
•     Hard to maintain: If you change the logic, you must update every copy of that code manually.
•     Difficult to read: Long programs without any structure become very hard to understand.
•     Difficult to debug: Finding the location of a bug in 500 lines of unstructured code is a nightmare.
 
Simple Analogy
Think of functions like the different departments in a company. The Accounts department handles all billing. The HR department handles all employee records. Each department does its own job independently. The manager (main program) just instructs each department (function) to do its task. This is exactly how functions work in Python.

 
1.2  What is a Function?
 
Definition: Function
A function is a named, self-contained block of statements that performs a specific task. It is written once and can be called (executed) any number of times from anywhere in the program. A function may optionally accept input values and may optionally return an output value to the caller.

 
1.3  Advantages of Functions
 
The advantages of using functions are:
1.    Code Reusability:  A function is written once and can be used as many times as needed. You do not have to rewrite the same logic every time you need it.
2.    Modularity:  A large, complex program is broken down into small, manageable pieces. Each piece (function) handles one specific task.
3.    Readability:  Code becomes easier to read and understand. A well-named function like calculate_area() immediately tells the reader what it does.
4.    Easy Debugging:  When a bug occurs, you can check one function at a time instead of searching through hundreds of lines of code.
5.    Easy Maintenance:  If the logic needs to change (e.g., a tax rate is updated), you change it in one place — inside the function — and the change applies everywhere automatically.
6.    Abstraction:  The caller does not need to know how the function works internally. You use print() every day without knowing how Python prints text to the screen.
7.    Teamwork:  In a large project, different programmers can write and test different functions independently and then combine them.
8.    Testing:  Each function can be tested individually with different inputs before being used in the full program.
 
2.  Defining and Calling a Function
 
2.1  How to Define a Function
 
In Python, we define (create) a function using the keyword def. The word def is short for define. Here is the complete syntax:
 
 General Syntax of a Function
def  function_name( parameters ) :
	"""Docstring — short description (optional but recommended)"""
	statement 1
	statement 2
	...
	return  value	# optional
 

 
Understanding each part of the syntax:
•     def:  This keyword tells Python that we are starting a function definition. It is always the first word.
•     function_name:  A name you choose for your function. It should be meaningful and describe what the function does. Use only lowercase letters and underscores (e.g., calculate_area, print_hello).
•     parameters:  These are the input variables listed inside the brackets. They are optional. If there are no inputs, the brackets are still required but left empty: ().
•     colon  ( : ):  The colon at the end of the def line is mandatory. It marks the beginning of the function body.
•     function body:  All the statements that make up the function. Every line of the body must be indented by exactly 4 spaces. Python uses indentation (not braces like C/Java) to identify which lines belong to the function.
•     return:  This sends a value back to the caller. It is optional. If omitted, the function returns None automatically.
 
 
 
 
2.2  Parameters vs. Arguments
Students often confuse these two terms. Here is the clear distinction:
 
Parameter
Argument
A variable listed inside the brackets in the function definition.
The actual value that is passed when the function is called.
It acts as a placeholder for the incoming value.
It is the real data that the function receives.
Example: in  def add(a, b):  — here a and b are parameters.
Example: in  add(10, 20)  — here 10 and 20 are arguments.
Lives only inside the function while it runs.
Comes from the calling code.

2.3  Calling a Function
Writing a function definition does not run the code inside it. The code inside the function runs only when you call the function. To call a function, write its name followed by brackets and any required arguments.
 
Definition vs. Call
Defining a function = Writing the recipe in a cookbook. Nothing is cooked yet.
Calling a function = Actually cooking the dish by following the recipe. This is when the code inside the function runs.

 
2.4  Your First Function — Step by Step
 
Let us write the simplest possible function and understand exactly how it works:
 
 Program 1 — Simplest Function
# Step 1: Define the function
def greet():
	print("Hello! Welcome to Python.")
	print("Have a great day!")
 
# Step 2: Call the function
greet()   	# First call
greet()   	# Second call — same function runs again!
 

 
 Output:
Hello! Welcome to Python.
Have a great day!
Hello! Welcome to Python.
Have a great day!

 
What happens step by step:
1.    Python reads the def line. It stores the function in memory. Nothing is printed yet.
2.    Python reaches greet() — the first call. It jumps into the function and executes the two print statements.
3.    The function ends. Python returns to the main program and continues to the next line.
4.    Python reaches greet() again — second call. The function runs once more, printing the same two lines.
3.  Indentation in Python
 
Indentation means adding spaces at the beginning of a line to show that it belongs to a particular block of code. In Python, indentation is not optional — it is a mandatory part of the language syntax.
 
Rules for indentation in functions:
•     Every statement inside a function must be indented by exactly 4 spaces from the left margin.
•     All lines in the function body must have the same indentation level.
•     When the indentation returns to the original level, Python understands that the function has ended.
•     If you mix tabs and spaces or forget to indent, Python raises an IndentationError.
 
Example of correct and incorrect indentation:
 
❌  INCORRECT
✅  CORRECT
def show():
def show():
print('Hi')   # No indent!
	print('Hi')   # 4 spaces OK
print('Bye')  # IndentationError
	print('Bye')  # 4 spaces OK
 
show()

 
EXAM IMPORTANT — Remember These Points
Python uses INDENTATION (spaces) to define blocks of code.
Every line inside a function must be indented by exactly 4 spaces.
C and Java use curly braces { } for blocks. Python uses indentation instead.
Forgetting indentation causes IndentationError — a very common beginner mistake.
Lines that are not indented belong to the main program, not to any function.

 4.  Scope and Lifetime of Variables
 4.1  What is Scope?
 
Definition: Scope
The scope of a variable is the part of the program where that variable can be accessed and used. A variable is not accessible everywhere in the program — it depends on where the variable was created.

 
Definition: Lifetime
The lifetime of a variable is the period of time during which the variable exists in the computer's memory — from when it is created to when it is automatically destroyed.

 
Simple Analogy
Think of a classroom. A whiteboard inside the classroom is visible only to students inside that class (local scope). A notice board in the college corridor is visible to everyone in the college (global scope). A variable inside a function is like the classroom whiteboard — accessible only inside that function.

 
4.2  Local Variables
 A variable created inside a function is called a local variable. It can only be used within that function.
 Properties of local variables:
•     A local variable is created when the function is called.
•     It exists only until the function finishes executing.
•     Once the function ends, the local variable is automatically deleted from memory.
•     It cannot be accessed from outside the function. If you try, Python raises a NameError.
•  Two different functions can have local variables with the same name — they are completely independent of each other.
 
 Program — Local Variable Example
def calculate_area(radius):
	pi = 3.14159      	# 'pi' is a LOCAL variable
	area = pi * radius * radius   # 'area' is also LOCAL
	print('Area:', area)
 
calculate_area(5)
 
# Try to access 'area' outside the function:
print(area)   # ERROR! NameError: name 'area' is not defined
 

 
 Output:
Area: 78.53975
NameError: name 'area' is not defined

 
4.3  Global Variables
 
A variable created outside all functions is called a global variable. It can be read by any function in the program.
 
Properties of global variables:
•     A global variable is created when the program starts and exists until the program ends.
•     It is accessible from anywhere in the program — inside any function or in the main code.
•     Any function can read a global variable freely — no special keyword is needed.
•     To modify a global variable inside a function, you must use the global keyword.
 
 Program — Global Variable Example
college_name = 'R. H. Sapat College'   # GLOBAL variable
city = 'Nashik'                     	# GLOBAL variable
 
def show_info():
	# Reading global variables — allowed without any keyword
	print('College:', college_name)
	print('City:', city)
 
def show_greeting():
	print('Welcome to', college_name)   # Can use global here too
 
show_info()
show_greeting()
 

 
 Output:
College: R. H. Sapat College
City: Nashik
Welcome to R. H. Sapat College

 
4.4  The global Keyword
 By default, if you try to assign a new value to a global variable inside a function, Python does NOT modify the original global variable. Instead, Python creates a brand new local variable with the same name. To actually modify the global variable from inside a function, you must declare it using the global keyword.
 Syntax: 
 Syntax of global keyword
def function_name():
	global variable_name
	variable_name = new_value   # Now this modifies the GLOBAL variable
 


 Program — global Keyword Example
count = 0	# Global variable
 
def increment():
	global count    	# Tell Python: use the GLOBAL 'count'
	count = count + 1
	print('Count inside function:', count)
 
increment()	# count becomes 1
increment()	# count becomes 2
increment()	# count becomes 3
print('Final count:', count)   # 3

 
 Output:
Count inside function: 1
Count inside function: 2
Count inside function: 3
Final count: 3

 
EXAM IMPORTANT — Remember These Points
Local variable — created inside a function, accessible only inside that function.
Global variable — created outside all functions, accessible everywhere.
To READ a global variable inside a function — no keyword needed.
To MODIFY a global variable inside a function — you MUST use the 'global' keyword.
If you assign to a global name inside a function without 'global', Python creates a NEW local variable. The original global is NOT changed.

4.5  Difference between Local and Global Variables 
Local Variable
Global Variable
Created inside a function.
Created outside all functions, at the top of the program.
Accessible only within that function.
Accessible from anywhere in the program.
Created when the function is called.
Created when the program starts.
Destroyed when the function finishes.
Destroyed when the program ends.
Cannot be accessed from outside the function.
Can be read by any function without any keyword.
Two functions can have local variables with the same name — they are separate.
Only one copy exists and it is shared by all functions.

 5.  The return Statement
5.1  What is the return Statement? 
Definition: return
The return statement is used inside a function to send a value back to the part of the program that called the function. When Python encounters a return statement, it immediately stops executing the function and sends the specified value to the caller.

 
Two things happen when return is executed:
•     The function stops executing immediately. Any statements below return in the same function are skipped.
•     The value written after return is sent back to the caller. The caller can store this value in a variable, print it, or use it in an expression.
 
 Program — return Statement
def add_numbers(a, b):
	result = a + b
	return result	# Send the result back to the caller
 
# The returned value is stored in variable 'total'
total = add_numbers(10, 20)
print('Sum is:', total)  	# Output: Sum is: 30
 
# The returned value can also be used directly
print(add_numbers(5, 3)) 	# Output: 8
 
# The returned value can be used in an expression
x = add_numbers(4, 6) * 2
print(x)                 	# Output: 20
 

 

5.2  Returning Multiple Values
 Python allows a function to return more than one value at the same time. The values are separated by commas after return. They are automatically packed into a tuple and the caller can unpack them into separate variables. 
 Program — Returning Multiple Values
def get_min_max(numbers):
	minimum = min(numbers)
	maximum = max(numbers)
	return minimum, maximum	# Returns two values
 
low, high = get_min_max([5, 2, 9, 1, 7])
print('Minimum:', low)	# Output: Minimum: 1
print('Maximum:', high)   # Output: Maximum: 9
 

 5.3  Difference between return and print
This is one of the most important concepts for beginners. print() and return look similar but they do very different things.
 
print statement
return statement
Displays a value on the screen for the user to see.
Sends a value back to the calling code for further use.
The value is shown on screen and then lost — it cannot be used further.
The value can be stored in a variable, used in calculations, or passed to another function.
The function still returns None even if it uses print.
The function returns whatever value is specified after return.
Example: def f(): print(5+3)   — shows 8 on screen.
Example: def f(): return 5+3   — sends 8 to the caller.
Useful when you just want to display a result.
Useful when the computed value is needed for further processing.
The caller gets None if they try to store the result.
The caller gets the actual computed value.

 
 Program — print vs return Comparison
# Function using print — result is displayed but cannot be used further
def add_with_print(a, b):
	print(a + b)    	# Shows the result but cannot be reused
 
result1 = add_with_print(5, 3)
print('Stored:', result1)   # Output: Stored: None  (not 8!)
 
# Function using return — result can be stored and reused
def add_with_return(a, b):
	return a + b    	# Sends result back to caller
 
result2 = add_with_return(5, 3)
print('Stored:', result2)   # Output: Stored: 8  (correct!)
doubled = result2 * 2
print('Doubled:', doubled)  # Output: Doubled: 16
 

 
 Output:
8
Stored: None
Stored: 8
Doubled: 16

 6.  Types of Functions 
Functions in Python are broadly divided into two types:
6.1  Built-in Functions 
Built-in Functions
Built-in functions are functions that are already written and provided by Python. You can use them directly in your program without writing any definition. These functions are available as soon as you start Python.

 Examples of commonly used built-in functions:
•     print()  —  Displays output on the screen.
•     input()  —  Takes input from the user.
•     len()  —  Returns the number of elements in a list, string, or tuple.
•     int(), float(), str()  —  Convert a value to integer, float, or string.
•     max(), min()  —  Return the largest or smallest value from a sequence.
•     sum()  —  Returns the sum of all elements in a list.
•     abs()  —  Returns the absolute (positive) value of a number.
•     range()  —  Generates a sequence of numbers.
•     sorted()  —  Returns a sorted version of a list.
•     type()  —  Returns the data type of a variable.
 6.2  User-Defined Functions 
User-Defined Functions
User-defined functions are functions that you write yourself using the def keyword to perform a specific task that your program needs. You define the name, parameters, and body of the function.

 User-defined functions are further classified into 4 types based on whether they have parameters and whether they return a value: 
Type 1 — No Parameter, No Return Value 
This type of function takes no input from the caller and does not return any value. It simply performs a task on its own (usually printing something). 
 Type 1 — No Parameter, No Return
def print_greeting():
	print("Hello! Welcome to FE Engineering.")
	print("Best of luck for your studies!")
 
print_greeting()   # Call the function
 

 
 Output:
Hello! Welcome to FE Engineering.
Best of luck for your studies!

 Type 2 — With Parameter, No Return Value 
This type accepts input through parameters but does not return any value. It performs the task and shows the result using print(). 
 Type 2 — With Parameter, No Return
def print_square(n):
	sq = n * n
	print('Square of', n, 'is', sq)
 
print_square(5)	# Output: Square of 5 is 25
print_square(9)	# Output: Square of 9 is 81
 

 
 Output:
Square of 5 is 25
Square of 9 is 81

 
Type 3 — No Parameter, With Return Value
 This type does not take any input but returns a value to the caller. It is used when the function generates a value on its own (e.g., reading user input or computing a constant). 
 Type 3 — No Parameter, With Return
def get_pi():
	return 3.14159
 
pi_value = get_pi()
area = pi_value * 7 * 7
print('Area of circle with radius 7:', area)
 

 
 Output:
Area of circle with radius 7: 153.93791

 
Type 4 — With Parameter, With Return Value (Most Common) 
This is the most commonly used type. It accepts input, performs computation, and sends the result back to the caller. 
 Type 4 — With Parameter, With Return (Most Common)
def add(a, b):
	result = a + b
	return result
 
total = add(10, 20)
print('Sum:', total)	# Output: Sum: 30
 

 
 Output:
Sum: 30

 
EXAM IMPORTANT — Remember These Points
Type 1: No parameter, No return — just performs a task (e.g., print a menu).
Type 2: Parameter, No return — receives input and displays result.
Type 3: No parameter, With return — generates and sends back a value.
Type 4: Parameter, With return — receives input, computes, and sends result back. (Most important type for exams.)

 7.  Default Arguments and Keyword Arguments
7.1  Default Arguments 
Sometimes you want a parameter to have a default value that is used automatically when the caller does not provide that argument. This is called a default argument. 
Rules for default arguments:
•     Default arguments are written in the function definition as parameter = default_value.
•     Default arguments must always be placed after non-default (required) arguments. You cannot place a default argument before a required one.
•     If the caller provides a value for the parameter, the provided value is used. If not, the default value is used.
 Program — Default Arguments
def greet(name, message='Good Morning'):
	print(message + ', ' + name + '!')
 
greet('Priya')                  	# Uses default message
greet('Rohan', 'Good Evening')  	# Overrides the default
 

 
 Output:
Good Morning, Priya!
Good Evening, Rohan!

 
7.2  Keyword Arguments 
Normally, arguments are matched to parameters by their position (first argument → first parameter, second → second, etc.). Python also allows you to pass arguments by name — these are called keyword arguments. When using keyword arguments, the order does not matter.
 
 Program — Keyword Arguments
def student_info(name, rollno, marks):
	print('Name:', name, '| Roll:', rollno, '| Marks:', marks)
 
# Positional — order matters
student_info('Ananya', 101, 88)
 
# Keyword — order does NOT matter
student_info(marks=92, name='Rohan', rollno=102)
 

 
 Output:
Name: Ananya | Roll: 101 | Marks: 88
Name: Rohan | Roll: 102 | Marks: 92

 8.  Lambda (Anonymous) Functions 
8.1  What is a Lambda Function? 
Definition: Lambda Function
A lambda function is a small, anonymous (nameless) function that is written in a single line. It is defined using the keyword lambda instead of def. It can accept any number of parameters but can only contain one expression. The value of that expression is automatically returned — no return keyword is needed.

 Syntax: 
 Lambda Syntax
variable = lambda  parameter1, parameter2 : expression
 

 
Analogy
Think of lambda as a quick, one-line version of a function. Just like you can send a short WhatsApp message instead of a long email when you need to say something simple — lambda is the short, quick version of a function for simple tasks.

 8.2  Lambda vs Regular Function 
Regular Function (def)
Lambda Function
Defined using the def keyword.
Defined using the lambda keyword.
Has a name.
Anonymous — has no name (unless stored in a variable).
Can have multiple statements in the body.
Can only have a single expression.
Uses an explicit return statement.
The expression is returned automatically — no return keyword.
Can have a docstring.
Cannot have a docstring.
Best for complex, multi-line logic.
Best for simple, one-line operations.

 
 Program — Lambda Examples
# Regular function to find square
def square(x):
	return x * x
 
# Equivalent Lambda function
square_lam = lambda x: x * x
 
print(square(5))    	# Output: 25
print(square_lam(5))	# Output: 25  (same result)
 
# Lambda with two parameters
add = lambda a, b: a + b
print(add(3, 7))    	# Output: 10
 
# Lambda with a condition
is_even = lambda n: 'Even' if n % 2 == 0 else 'Odd'
print(is_even(4))   	# Output: Even
print(is_even(7))   	# Output: Odd
 

 
9.  Documentation Strings (Docstrings) 
Definition: Docstring
A docstring (documentation string) is a special string written as the very first statement inside a function. It is enclosed in triple double-quotes """....""". Its purpose is to explain what the function does, what inputs it expects, and what it returns.

 
Why are docstrings important?
•     They serve as built-in documentation for your function. Anyone reading the code can understand the function without reading all its internal logic.
•     Python stores the docstring as a special attribute of the function, which can be accessed using function_name.__doc__ or help(function_name).
•     Code editors like VS Code show the docstring as a popup hint when you start typing the function name.
•     It is a professional programming standard. Industry-level Python code always includes docstrings.
•     Your future self (and your teammates) will understand the function without having to re-read every line of code.
 
9.1  Single-Line Docstring 
 Single-Line Docstring
def square(n):
	"""Return the square of the number n."""
	return n * n
 
def is_even(n):
	"""Return True if n is even, False otherwise."""
	return n % 2 == 0
 
# Accessing the docstring
print(square.__doc__)	# Output: Return the square of the number n.
help(is_even)        	# Displays formatted documentation
 

 
9.2  Multi-Line Docstring 
For functions with multiple parameters and complex behaviour, a multi-line docstring is written. The opening """ is on the first line after def, and the closing """ is on a separate line after all the description.
 
 Multi-Line Docstring
def calculate_simple_interest(principal, rate, time):
	"""
	Calculate and return the simple interest.
	
	Parameters:
    	principal (float): The initial amount of money.
    	rate (float): Annual interest rate in percentage.
    	time (float): Time period in years.
	
	Returns:
    	float: The simple interest amount.
	
	Example:
    	>>> calculate_simple_interest(1000, 5, 2)
    	100.0
	"""
	interest = (principal * rate * time) / 100
	return interest
 
si = calculate_simple_interest(5000, 8, 3)
print('Simple Interest:', si)   # Output: 1200.0


Docstring Template to Follow
First line: One sentence describing what the function does.
Parameters section: List each parameter with its type and meaning.
Returns section: Describe what the function returns.
Example section: Show a sample call and its expected output.

 10.  Good Programming Practices Using Functions
 Writing a function that works correctly is the first step. Writing a function that is clean, readable, and maintainable is what makes you a good programmer. The following practices are followed by professional Python developers worldwide.
 Practice 1 — Use Meaningful Names
 Always choose names for functions and variables that clearly describe their purpose.
•     Use lowercase letters with underscores between words. This is called snake_case. Example: calculate_area, find_maximum.
•     Function names should start with a verb (action word) that describes what the function does. Good examples: get_name(), print_bill(), check_password().
•     Avoid meaningless names like f(), x1(), fn2(). Someone reading your code should understand its purpose from the name alone. 
Practice 2 — One Function = One Task 
Each function should do exactly one specific task and do it well. If you need to use the word 'and' to describe what a function does, it is probably doing too much and should be split into two separate functions. 
❌  INCORRECT
✅  CORRECT
# BAD: One function does everything
# GOOD: Each function does one job
def process(name, marks):
def get_average(marks):
	avg = sum(marks)/len(marks)
	return sum(marks)/len(marks)
	grade = 'P' if avg>=40 else 'F'
 
	print(name, avg, grade)
def get_grade(avg):
	# Too many responsibilities!
	return 'P' if avg>=40 else 'F'
 
 
 
def display(name,avg,grade):
 
	print(name, avg, grade)

 Practice 3 — Always Write a Docstring
•     Every function you write should have at least a one-line docstring. Even if it seems obvious to you now, it will save time for anyone (including yourself) who reads the code later.
•     A docstring is not the same as a comment. Comments explain the code. Docstrings document the function's purpose, parameters, and return value.
 Practice 4 — Use return Instead of Global Variables 
Avoid modifying global variables inside functions whenever possible. Instead, return the computed value from the function and let the caller store it. 
❌  INCORRECT
✅  CORRECT
# BAD: Using global unnecessarily
# GOOD: Using return
result = 0
 
 
def add(a, b):
def add(a, b):
	return a + b
	global result
 
	result = a + b
 
 
result = add(5, 3)
add(5, 3)
print(result)
print(result)
 

 Practice 5 — Keep Functions Short 
•  A function should ideally be short enough to fit on one screen — roughly 20 to 30 lines maximum.
•     If a function is getting too long, it is a signal that you should break it into smaller helper functions.
•     Short functions are easier to read, test, and debug.
Practice 6 — Test Your Function with Multiple Inputs 
•     Before using a function in a large program, test it independently with different values — including normal inputs, boundary values (like 0), and extreme values.
•     Use Python's assert statement for quick testing: assert square(5) == 25.
•     Testing every function individually (called unit testing) makes it much easier to find and fix bugs.
 
EXAM IMPORTANT — Remember These Points
Use snake_case names that start with a verb: calculate_tax(), find_max().
One function = one task. Do not mix multiple responsibilities in one function.
Always write a docstring for every function.
Prefer return over global variables — it makes functions predictable and reusable.
Keep functions short — around 20 lines maximum. If longer, break into smaller functions.
Test functions individually with different inputs before using them in the full program.

 

11.  Simple Programs Using Functions 
The following programs cover all the basic topics and are ideal for practice. Study each one carefully, understand how the function is defined and called, and try to write them yourself without looking at the solution.
Program 1 — Addition of Two Numbers
 Program 1 — Addition
def add(a, b):
	"""Return the sum of two numbers."""
	return a + b
 
x = int(input('Enter first number: '))
y = int(input('Enter second number: '))
result = add(x, y)
print('Sum:', result)

 Program 2 — Square of a Number
 Program 2 — Square
def square(n):
	"""Return the square of n."""
	return n * n
 
num = int(input('Enter a number: '))
print('Square:', square(num))
 

 Program 3 — Swap Two Numbers
 Program 3 — Swap
def swap(a, b):
	"""Return the two values swapped."""
	return b, a	# Return b first, then a
 
x = 10
y = 20
print('Before swap: x =', x, ', y =', y)
x, y = swap(x, y)
print('After swap:  x =', x, ', y =', y)
 

 
 Output:
Before swap: x = 10 , y = 20
After swap:  x = 20 , y = 10

 Program 4 — Find Maximum of Three Numbers
 Program 4 — Maximum of Three
def maximum(a, b, c):
	"""Return the largest of three numbers."""
	if a >= b and a >= c:
    	return a
	elif b >= a and b >= c:
    	return b
	else:
    	return c
 
a = int(input('Enter first number: '))
b = int(input('Enter second number: '))
c = int(input('Enter third number: '))
print('Maximum:', maximum(a, b, c))

 Program 5 — Check Even or Odd
 Program 5 — Even or Odd
def check_even_odd(n):
	"""Return "Even" if n is even, "Odd" otherwise."""
	if n % 2 == 0:
    	return "Even"
	else:
    	return "Odd"
 
num = int(input('Enter a number: '))
print(num, 'is', check_even_odd(num))
 

 Program 6 — Factorial of a Number
 Program 6 — Factorial
def factorial(n):
	"""Return the factorial of n (n!)."""
	fact = 1
	for i in range(1, n + 1):
    	fact = fact * i
	return fact
n = int(input('Enter a number: '))
print('Factorial of', n, '=', factorial(n))


 Output:
Enter a number: 5
Factorial of 5 = 120

 
Program 7 — Check Prime Number
 Program 7 — Prime Number Check
def is_prime(n):
	"""Return True if n is prime, False otherwise."""
	if n < 2:
    	return False
	for i in range(2, n):
    	if n % i == 0:
        	return False
	return True
 
num = int(input('Enter a number: '))
if is_prime(num):
	print(num, 'is a Prime number.')
else:
	print(num, 'is NOT a Prime number.')
 

 Program 8 — Reverse a String
 Program 8 — Reverse String
def reverse_string(s):
	"""Return the reverse of a string."""
	return s[::-1]   # Slicing with step -1 reverses the string
 
text = input('Enter a string: ')
print('Reversed:', reverse_string(text))
 

 Program 9 — Check Palindrome (String)
 Program 9 — Palindrome Check
def is_palindrome(s):
	"""Return True if the string is a palindrome."""
	s = s.lower()       	# Convert to lowercase for comparison
	return s == s[::-1] 	# Compare string with its reverse
 
word = input('Enter a word: ')
if is_palindrome(word):
	print(word, 'IS a palindrome.')
else:
	print(word, 'is NOT a palindrome.')
 

 Program 10 — Count Vowels in a String
 Program 10 — Count Vowels
def count_vowels(s):
	"""Return the count of vowels in the string."""
	count = 0
	for ch in s.lower():
    	if ch in 'aeiou':
        	count = count + 1
	return count
 
text = input('Enter a string: ')
print('Number of vowels:', count_vowels(text))

 Program 11 — Simple Interest using Function
 Program 11 — Simple Interest
def simple_interest(p, r, t):
	"""Return simple interest for given principal, rate, and time."""
	si = (p * r * t) / 100
	return si
 
p = float(input('Principal amount: '))
r = float(input('Rate of interest: '))
t = float(input('Time in years: '))
interest = simple_interest(p, r, t)
print('Simple Interest: Rs', interest)
print('Total Amount:	Rs', p + interest)
 

 Program 12 — Armstrong Number Check
 Program 12 — Armstrong Number
def is_armstrong(n):
	"""Return True if n is an Armstrong number."""
	digits = str(n)       	# Convert number to string to access each digit
	power = len(digits)   	# Number of digits
	total = 0
	for d in digits:
    	total = total + int(d) ** power
	return total == n
 
num = int(input('Enter a number: '))
if is_armstrong(num):
	print(num, 'is an Armstrong number.')
else:
	print(num, 'is NOT an Armstrong number.')
 

 
 Output:
Enter a number: 153
153 is an Armstrong number.

 12.  Practice Problems 
Answer the following questions in your notebook. Write the program, test it, and note down the output. All questions carry 5 marks each unless mentioned otherwise. 
Write the Following Programs Using Functions 
Q.1
5 Marks
5 Marks
Write a function called power(base, exp) that accepts two numbers and returns base raised to the power exp (i.e., base^exp). Do NOT use Python's built-in ** operator or pow() function. Use a loop to compute the answer. Call the function for (2, 10), (3, 5), and (5, 3).

  
Q.2
5 Marks
5 Marks
Write a function sum_of_digits(n) that takes a positive integer and returns the sum of all its digits. For example, sum_of_digits(1234) should return 10 (1+2+3+4). Include a proper single-line docstring.

 
Q.3
5 Marks
5 Marks
Write a function count_words(sentence) that accepts a sentence as a string and returns the number of words in it. For example, count_words('Python is easy') should return 3. Test with at least three different sentences.

 
Q.4
5 Marks
5 Marks
Write a function celsius_to_fahrenheit(c) that converts Celsius to Fahrenheit (Formula: F = C x 9/5 + 32) and returns the result. Then write another function fahrenheit_to_celsius(f) for the reverse conversion. Call both functions and print the results.

 
Q.5
5 Marks
5 Marks
Write a function is_palindrome_number(n) that returns True if the number n reads the same forwards and backwards (e.g., 121, 1331, 12321), and False otherwise. Do NOT convert the number to a string — find the reverse mathematically using loops.


Q.6
5 Marks
5 Marks
Write a function print_pattern(n) that takes a number n and prints a right-angle triangle pattern of stars. For n=4, the output should be: Row 1 has 1 star, Row 2 has 2 stars, Row 3 has 3 stars, Row 4 has 4 stars. Each row is on a new line.

  
Q.7
5 Marks
5 Marks
Write a function string_info(s) that accepts a string and returns four values: (1) total length, (2) number of uppercase letters, (3) number of lowercase letters, (4) number of digits. Call the function and unpack all four returned values into separate variables.

  
Q.8
5 Marks
5 Marks
Using lambda and map(), write a program that takes a list of temperatures in Celsius and converts all of them to Fahrenheit in a single line using map() and lambda. Print the original list and the converted list. Also, use filter() with lambda to keep only those temperatures that are above 37 degrees Celsius (body temperature).

 
Q.9
8 Marks
8 Marks
Write a complete Student Result System using functions only. Include: (a) get_grade(marks) — returns letter grade O/A+/A/B/C/F based on percentage. (b) compute_result(name, marks_list) — calculates total, percentage, grade, and pass/fail status (pass = all marks >= 35). (c) display_result(name, total, percentage, grade, status) — prints a formatted result card. Call these functions for three different students and display their result cards.

  
Q.10
8 Marks
8 Marks
Write a function fibonacci(n) that returns a list containing the first n Fibonacci numbers. (Fibonacci series: 0, 1, 1, 2, 3, 5, 8 ...). Include a multi-line docstring explaining parameters and return value. Then write a second function is_fibonacci(num) that checks whether a given number is part of the Fibonacci series. Test both functions.

  13.  Viva and Exam Questions 
Q1. What is a function? What are its advantages?
• 	A function is a named, self-contained block of statements that performs a specific task. It is defined once and can be called any number of times.
• 	Advantage 1 — Code Reusability: Write the logic once and reuse it as many times as needed.
• 	Advantage 2 — Modularity: A large program is broken into small, manageable pieces.
• 	Advantage 3 — Readability: Well-named functions make code easy to understand.
• 	Advantage 4 — Easy Debugging: You can test and fix one function at a time.
• 	Advantage 5 — Easy Maintenance: A change inside one function is automatically applied everywhere it is called.


Q2. What is the difference between a parameter and an argument?
• 	A parameter is the variable listed inside the brackets in the function definition. It is a placeholder.
• 	An argument is the actual value passed to the function when it is called.
• 	Example: In  def add(a, b):  — here a and b are parameters.
• 	In  add(10, 20)  — here 10 and 20 are arguments.
• 	Parameters exist only during the function's execution. Arguments come from the calling code.


Q3. What is scope? Explain local and global scope.
• 	Scope is the part of the program where a variable can be accessed and used.
• 	A local variable is created inside a function and is accessible only within that function.
• 	A local variable is destroyed when the function finishes executing.
• 	A global variable is created outside all functions and is accessible from anywhere in the program.
• 	A global variable exists for the entire duration of the program.
• 	If you try to access a local variable from outside the function, Python raises a NameError.

 
Q4. What is the global keyword? When is it used?
• 	The global keyword is used inside a function to tell Python that a variable refers to the global variable, not a new local one.
• 	It is needed when you want to MODIFY a global variable from inside a function.
• 	Without global, any assignment inside a function creates a new local variable, leaving the global unchanged.
• 	You do NOT need the global keyword if you only want to read (not modify) a global variable.

 
Q5. What is the return statement? What is the difference between return and print?
• 	The return statement sends a value from the function back to the calling code.
• 	When return is executed, the function immediately stops and sends the specified value to the caller.
• 	Difference 1: print only displays the value on screen — the caller cannot use that value further. return sends the value to the caller who can store it and use it.
• 	Difference 2: A function that uses only print still returns None to the caller.
• 	Difference 3: return is used when the computed value is needed for further calculations. print is used when you only want to show the result.
• 	Example: result = add(5, 3) works only if add() uses return, not print.

 
Q6. What are the four types of user-defined functions?
• 	Type 1 — No parameter, No return: The function takes no input and returns nothing. Example: def print_menu(): print('1. Add').
• 	Type 2 — With parameter, No return: The function takes input through parameters but does not return any value. It displays results using print(). Example: def show_square(n): print(n*n).
• 	Type 3 — No parameter, With return: The function takes no input from the caller but returns a value. Example: def get_pi(): return 3.14159.
• 	Type 4 — With parameter, With return (most common): The function takes input and returns a computed result. Example: def add(a,b): return a+b.

 
Q7. What is a lambda function? How is it different from a regular function?
• 	A lambda function is a small, anonymous (nameless) function defined using the lambda keyword in a single line.
• 	Syntax: variable = lambda parameters : expression
• 	Difference 1: Lambda uses lambda keyword; regular function uses def keyword.
• 	Difference 2: Lambda is anonymous — it has no name. Regular functions must have a name.
• 	Difference 3: Lambda can only contain one expression. Regular functions can have multiple statements.
• 	Difference 4: Lambda automatically returns the expression value. Regular functions need an explicit return statement.
• 	Lambda is mostly used with map(), filter(), and sorted() for short, throwaway operations.

 
Q8. What is a docstring? How do you access it?
• 	A docstring (documentation string) is a special string written as the very first statement inside a function, enclosed in triple double-quotes.
• 	Its purpose is to describe what the function does, its parameters, and its return value.
• 	It is stored as a special attribute called __doc__ on the function object.
• 	You can access it using:  function_name.__doc__  or  help(function_name).
• 	Docstrings are important because they serve as built-in documentation and are shown as hints in code editors.
• 	They are a professional programming standard and must be written for every function in industry-level code.

 
Q9. What is indentation in Python? Why is it important?
• 	Indentation means adding spaces at the beginning of a line to show that it belongs to a particular block of code.
• 	In Python, indentation is MANDATORY — it is how Python determines which statements belong to a function (or loop, or condition).
• 	Every line inside a function must be indented by exactly 4 spaces.
• 	Unlike C or Java which use curly braces { } to define blocks, Python uses indentation.
• 	If you forget indentation or use inconsistent spacing, Python raises an IndentationError and the program does not run.
• 	Consistent indentation also makes the code visually clean and easy to read.

 
Q10. What is the difference between built-in functions and user-defined functions?
• 	Built-in functions are already provided by Python. They are available immediately without writing any definition. Examples: print(), input(), len(), max(), min(), sum(), range().
• 	User-defined functions are written by the programmer using the def keyword to solve a specific problem.
• 	Built-in functions are tested and optimised by Python's developers. They are reliable and fast.
• 	User-defined functions are written as per the requirements of the program.
• 	You do not need to know how built-in functions work internally — you just call them. User-defined functions are written, maintained, and tested by you.

 

 14.  Quick Revision Summary 
Key Points to Revise Before the Exam: 
1.    Function: A named block of code that performs a specific task. Defined using the def keyword. Called by writing function_name().
2.    Parameter vs Argument: Parameter is the variable in the definition (placeholder). Argument is the actual value passed during the call.
3.    Indentation: Mandatory in Python. All lines inside a function must be indented by exactly 4 spaces.
4.    Local Variable: Created inside a function. Accessible only within that function. Destroyed when function ends.
5.    Global Variable: Created outside all functions. Accessible everywhere. Use the global keyword to modify it inside a function.
6.    return statement: Sends a value back to the caller. Exits the function immediately. Without return, function returns None.
7.    return vs print: print shows the value on screen but the caller gets None. return sends the actual value to the caller for further use.
8.    Type 1: No parameter, No return — just performs a fixed task.
9.    Type 2: With parameter, No return — receives input, uses print to show result.
10. Type 3: No parameter, With return — generates and sends back a value.
11. Type 4: With parameter, With return — most common type. Takes input, computes, returns result.
12. Default Arguments: Parameters with preset values. Default args must come after non-default args.
13. Lambda: Anonymous one-line function. Syntax: lambda params : expression. Used with map(), filter(), sorted().
16. Docstring: Triple-quoted string as first statement in function. Access using function_name.__doc__ or help().
17. Good Practices: Use meaningful names, one function = one task, write docstrings, prefer return over globals, keep functions short.
 

