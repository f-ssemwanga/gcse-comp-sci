Programming Basics: Inputs, Outputs & Structured Programming
Year 10 GCSE Computer Science (AQA Specification)
What You'll Learn
By the end of this lesson, you will be able to:

Write Python programs using variables, input/output and subroutines
Apply type casting to convert between data types
Use proper commenting and documentation in your code
Create modular programs with multiple subroutines


Prerequisites

Basic understanding of what programming is
Access to Thonny IDE or Python environment
Willingness to experiment and make mistakes!


Key Concepts
1. Comments
Comments help explain your code to others (and your future self):
python# This is a single line comment

"""
This is a multi-line comment
Used for longer explanations
"""
2. Variables and Assignment
Variables store data that your program can use:
pythonage = 14
name = "Dave"
pi = 3.14159
3. User Input
The input() function gets data from the user:
pythonname = input("What should I call you? ")
# Note: ALL input is treated as a string!
4. Output and Concatenation
Display information to the user:
python# Traditional concatenation
print(name + " is " + str(age))

# F-string method (preferred)
print(f"{name} is {age}")
5. Type Casting
Convert between data types when needed:
pythonage_string = input("How old are you? ")
age_number = int(age_string)  # Convert to integer
result = age_number + 1  # Now we can do math!
6. Subroutines (Functions)
Organize code into reusable blocks:
pythondef greet_user():
    """This function greets the user"""
    name = input("What's your name? ")
    print(f"Hello, {name}!")

# Call the function
greet_user()

Guided Practice Tasks
Task 1: Basic Program Structure
Create a simple program that demonstrates the core concepts:
pythondef comments_test():
    """We are experimenting with comments and variables"""
    
    # Variable assignment
    age = 14
    name = "Dave"
    
    """
    This is a multi-line comment
    Used for longer explanations
    """
    
    # Output using f-strings
    print(f"{name} is {age}")

# Call the function
comments_test()
Your Turn: Modify this program to use your own name and age.
Task 2: User Input Practice
Enhance the program to get information from the user:
pythondef user_input_demo():
    """Demonstrates getting input from users"""
    
    name = input("What should I call you? ")
    age_string = input("How old are you? ")
    
    # Convert string to integer for calculations
    age = int(age_string)
    
    print(f"{name} will be {age + 1} in a year's time")

user_input_demo()
Your Turn: Add another input that asks for the user's favorite color and include it in the output.
Task 3: Multiple Subroutines
Create a program with separate functions for different tasks:
pythondef get_user_info():
    """Gets user's name and age"""
    name = input("What's your name? ")
    age = int(input("How old are you? "))
    return name, age

def display_info(name, age):
    """Displays formatted user information"""
    print(f"Hello {name}!")
    print(f"You are {age} years old")
    print(f"Next year you'll be {age + 1}")

def main():
    """Main program that coordinates everything"""
    name, age = get_user_info()
    display_info(name, age)

# Run the program
main()
Your Turn: Add a third function that calculates and displays something interesting about the user's age (like how many days old they are).

Programming Challenges
Challenge 1: Digital Dice
Difficulty: ⭐⭐
Write a program that outputs a virtual dice showing the number 5:
○○○○○○○○○○○○
○ ●  ●  ● ○
○           ○
○ ●  ●  ● ○
○           ○
○ ●  ●  ● ○
○○○○○○○○○○○○
Requirements:

Use a subroutine
Include docstring explaining what the program does
Add appropriate comments

<details>
<summary>Hint</summary>
Use multiple print statements with the same characters repeated.
</details>
Challenge 2: ASCII Art Name
Difficulty: ⭐⭐⭐
Write a program that outputs your name in digital/ASCII art style.
Example Output:
My name in digital art looks like:

FRANCIS
Requirements:

Ask user for their name
Display it in ASCII art format
Use subroutines to organize your code
Include proper documentation

<details>
<summary>Hint</summary>
Research "Text to ASCII art generators" for inspiration, then recreate the pattern in Python.
</details>
Challenge 3: Simple Adder
Difficulty: ⭐⭐
Create a program that asks for two numbers and outputs their sum.
Example Output:
You have entered numbers 5 and 12
The sum of 5 and 12 is 17
Requirements:

Use appropriate type casting
Format output clearly
Include input validation (advanced)

Challenge 4: Test Marks Calculator
Difficulty: ⭐⭐⭐
Write a program that asks for three test marks and calculates the average.
Example Output:
The 3 test marks you entered were: 46, 67 and 88
The Average of your 3 test marks is 67
Requirements:

Use subroutines for input, calculation, and output
Handle the math correctly
Format output professionally

Challenge 5: Toy Car Worker Wage Calculator
Difficulty: ⭐⭐⭐
A worker gets paid £9/hour plus £0.60 for every toy car they make. Calculate their daily wage.
Example Output:
You worked 7.5 hours
You produced 25 toy trains
Your day's wage is £67.50
Requirements:

Get hours worked and items produced from user
Calculate total wage correctly
Display result with proper currency formatting

Challenge 6: Volume Calculator
Difficulty: ⭐⭐⭐
Calculate the volume of a box given its dimensions.
Example Output:
The volume of your box which is 120cm by 80cm by 50cm is 480,000 cubic centimetres
Requirements:

Ask for length, width, and height
Calculate volume (length × width × height)
Format large numbers with commas

Challenge 7: Pocket Money Calculator
Difficulty: ⭐⭐⭐⭐
Track weekly expenses and calculate remaining pocket money.
Example Output:
This week you spend £--- on your phone bill, £--- on food, £--- on seeing friends
You had £--- in your account, now you have £--- left
Requirements:

Ask for weekly pocket money amount
Get costs for phone, food, and social activities
Calculate and display remaining money
Handle negative balances appropriately


Self-Assessment Checklist
Basic Level

 Can write simple programs with variables
 Uses comments to explain code
 Gets input from users successfully
 Displays output using print statements
 Calls subroutines correctly

Developing Level

 Uses type casting appropriately
 Formats output using f-strings
 Creates multiple subroutines
 Includes proper docstrings
 Handles basic calculations

Advanced Level

 Implements input validation
 Uses return values effectively
 Creates modular, well-organized code
 Adds creative enhancements
 Helps other students debug their code


Extension Activities
For Quick Finishers

Code Golf: Rewrite one of your programs using the fewest lines possible
Error Handling: Add try/except blocks to handle invalid input
Documentation Master: Create detailed comments explaining every line
Creative Enhancement: Add ASCII art, colors, or interactive features

Research Tasks

Look up Python's format() method as an alternative to f-strings
Research the random module to add randomness to your programs
Investigate how to validate user input more robustly
Explore Python's built-in math module for advanced calculations


Common Mistakes and Debugging Tips
Problem: "NameError: name 'x' is not defined"
Solution: Make sure you've spelled variable names correctly and defined them before using them.
Problem: "TypeError: unsupported operand type(s)"
Solution: You're probably trying to do math with strings. Use int() or float() to convert input.
Problem: "SyntaxError: invalid syntax"
Solution: Check for missing colons : after function definitions, missing quotes around strings, or incorrect indentation.
Problem: Function doesn't run
Solution: Make sure you're calling the function with function_name() after defining it.

Using Thonny IDE
Thonny is your main programming environment for this course. Here's how to use it effectively:
Getting Started

Open Thonny on your device
Create a new file: File → New (or Ctrl+N)
Save your work: File → Save As... (give it a meaningful name like lesson1_basics.py)

Running Your Code

Green Play Button: Click to run your entire script (or press F5)
Python Shell: The bottom panel shows output and allows quick testing
Unsaved Warning: Files show as "untitled" until saved - save regularly!

Helpful Features

Syntax Highlighting: Different colors help you spot errors
Assistant Panel: Provides helpful error explanations and suggestions
Line Numbers: Help you locate errors quickly
Auto-indent: Thonny helps format your code correctly

Debugging Tips

Use the Step Through feature to see your code run line by line
Check the Variables panel to see what's stored in memory
The Assistant will explain error messages in plain English


Additional Resources
For Extra Practice

Python Sponge - Interactive Python exercises perfect for beginners
Codecademy Python Course - Free interactive lessons
Python.org Beginner's Guide - Official Python documentation

Reference Materials

Python.org Official Tutorial - Comprehensive guide
Real Python Beginner Guides - In-depth articles and tutorials
Automate the Boring Stuff - Free online book for practical Python

Video Tutorials

Python for Beginners - Microsoft - Step-by-step video series
Corey Schafer Python Tutorials - Clear explanations of Python concepts