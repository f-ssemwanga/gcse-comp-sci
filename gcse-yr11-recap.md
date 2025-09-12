# GCSE Computer Science Year 11 Recap Tasks

## AQA Specification Skills Review

### Essential Programming Concepts - Quick Reference

#### Variables and Data Types

``` python
age = 16              # integer
height = 5.8          # float/real
name = "Alice"        # string
is_student = True     # boolean
```

#### Input and Output

``` python
name = input("Enter your name: ")
print("Hello", name)
print(f"You are {age} years old")
```

#### String Manipulation

``` python
first_name = "John"
surname = "Smith"
full_name = first_name + " " + surname    # concatenation
username = first_name[0:3]                # slicing (first 3 chars)
name_length = len(first_name)             # length
```

#### Selection (IF statements)

``` python
if score >= 70:
    print("Pass")
else:
    print("Fail")

if age >= 16 and has_licence == True:
    print("Can drive")
```

#### Iteration (Loops)

``` python
# FOR loop - count 5 times
for i in range(5):
    print("Question", i+1)

# WHILE loop - repeat until condition false
while speed < 10 or speed > 50:
    speed = int(input("Enter speed (10-50): "))
```

#### Functions

``` python
def calculate_area(length, width):
    area = length * width
    return area

# Call the function
result = calculate_area(5, 3)
```

#### Validation Patterns

``` python
# Range check
while number < 1 or number > 100:
    number = int(input("Enter 1-100: "))

# Presence check
while name == "":
    name = input("Name cannot be empty: ")
```

#### Mathematical Operations

``` python
total = 10 + 5        # addition
remainder = 17 % 5    # modulo (gives 2)
whole_division = 17 // 5    # integer division (gives 3)
```

------------------------------------------------------------------------

## Programming Challenge Tasks

### 🏆 Challenge 1: Rectangle Perimeter Calculator

**Difficulty: ⭐**

Write an algorithm that calculates the perimeter of a rectangle.

**Requirements:** - Allow user to enter height and width of rectangle -
Calculate and output the perimeter - Use appropriate variable names

**Hints:** - Remember the formula for rectangle perimeter - Consider
what data type is most appropriate - Think about meaningful variable
names

------------------------------------------------------------------------

### 🏆 Challenge 2: Username Generator

**Difficulty: ⭐⭐**

Create a username generator for new students logging onto the school
system.

**Requirements:** - Get user's first name and surname - Generate
username using first 3 letters of first name + first 3 letters of
surname - Output the generated username - Assume names have at least 3
characters

**Hints:** - You'll need string manipulation techniques - Think about
how to extract parts of strings - Consider converting to lowercase for
consistency

------------------------------------------------------------------------

### 🏆 Challenge 3: Interactive Quiz System

**Difficulty: ⭐⭐⭐**

Design a quiz program with multiple choice questions.

**Requirements:** - Create exactly 5 questions with multiple choice
options - Check if user's answer is correct - Provide feedback for each
question - Keep track of score throughout - Display final score at the
end

**Hints:** - You'll need a way to track the running total - Consider how
to store the correct answers - Think about how to compare user input
with correct answers - Plan your question format carefully

------------------------------------------------------------------------

### 🏆 Challenge 4: Go-kart Braking Calculator

**Difficulty: ⭐⭐⭐**

Calculate braking distance for go-karts at different speeds and
conditions.

**Requirements:** - Repeatedly ask for speed until user enters value
between 10-50 km/h (inclusive) - Calculate braking distance by dividing
speed by 5 - Ask if ground is wet (expect 'yes' response for wet
conditions) - If wet, multiply braking distance by 1.5 - Output final
braking distance

**Hints:** - You'll need input validation with a loop - Think about the
order of calculations - Consider how to check for the wet ground
condition - Plan your variable names before you start

------------------------------------------------------------------------

### 🏆 Challenge 5: Hexadecimal Converter (Extension)

**Difficulty: ⭐⭐⭐⭐**

Create a function that converts decimal numbers to hexadecimal.

**Requirements:** - Function name: convertToHEX - Takes single integer
parameter - Only works for values 0-255 - Returns "Cannot convert" for
invalid ranges - Returns 2-character hexadecimal string for valid
inputs - Must be a proper function that returns values

**Hints:** - Research hexadecimal number system (base 16) - Think about
the conversion algorithm or built-in functions - Consider how to format
the output correctly - Remember functions should return, not print

------------------------------------------------------------------------

## ✅ Success Criteria Checklist

For each task, ensure your solution includes: - Functionality: Program
works as specified - Validation: Appropriate input checking where
needed - Variables: Meaningful names following conventions - Structure:
Clear, readable code with proper indentation - Comments: Brief
explanations for complex sections - Testing: Try different inputs to
verify correctness

------------------------------------------------------------------------

## 🚀 Extension Opportunities

-   Add error handling for unexpected inputs
-   Improve user interface with clear prompts and formatting
-   Consider edge cases and unusual inputs
-   Think about code efficiency and readability
