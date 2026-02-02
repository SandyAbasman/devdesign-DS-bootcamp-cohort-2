# Python Learning Summary - Data Science Bootcamp Cohort 2

A comprehensive beginner-friendly guide to all Python concepts covered in the bootcamp.

---

## Table of Contents

1. [Week 3 - Python Basics](#week-3---python-basics)
   - [Variables](#variables)
   - [Numbers](#numbers)
   - [Strings](#strings)
   - [Math Operations](#math-operations)
   - [User Input](#user-input)

2. [Week 4 - Control Flows](#week-4---control-flows)
   - [Comparison Operators](#comparison-operators)
   - [Logical Operators](#logical-operators)
   - [If/Else Statements](#ifelse-statements)
   - [Input Validation](#input-validation)

3. [Week 4 - Lists](#week-4---lists)
   - [List Introduction](#list-introduction)
   - [Accessing List Items](#accessing-list-items)
   - [List Slicing](#list-slicing)
   - [List Operations](#list-operations)

4. [Week 4 - Loops](#week-4---loops)
   - [For Loops](#for-loops)
   - [While Loops](#while-loops)
   - [Break Statement](#break-statement)
   - [Continue Statement](#continue-statement)

5. [Week 5 - Dictionaries](#week-5---dictionaries)
   - [Dictionary Introduction](#dictionary-introduction)
   - [Accessing Dictionary Values](#accessing-dictionary-values)
   - [Dictionary Methods](#dictionary-methods)
   - [Dictionary Operations](#dictionary-operations)

6. [Week 5 - Working with Files](#week-5---working-with-files)
   - [File Introduction](#file-introduction)
   - [Reading from Files](#reading-from-files)
   - [Reading File Lines](#reading-file-lines)
   - [Writing to Files](#writing-to-files)
   - [Appending to Files](#appending-to-files)
   - [Processing CSV Data](#processing-csv-data)

7. [Week 6 - Functions](#week-6---functions)
   - [Function Introduction](#function-introduction)
   - [Return Values](#return-values)
   - [Default Parameters](#default-parameters)
   - [Positional and Keyword Arguments](#positional-and-keyword-arguments)
   - [Return Multiple Values](#return-multiple-values)
   - [Variable Scope](#variable-scope)

8. [Week 7 - Advanced Working with Files](#week-7---advanced-working-with-files)
   - [Reading from CSV Files](#reading-from-csv-files)
   - [Writing to CSV Files](#writing-to-csv-files)
   - [CSV Quotes](#csv-quotes)
   - [Working with OS Module](#working-with-os-module)
   - [Directory Utilities](#directory-utilities)

---

## Week 3 - Python Basics

### Variables

**What are Variables?**

Think of variables as labeled boxes where you store information. Just like you might label a box "Books" or "Clothes", variables have names and store values. The name helps you remember what's inside, and you can change what's inside whenever you need to.

**How to Create Variables**

In Python, creating a variable is simple: you write the variable name, an equals sign (`=`), and then the value you want to store.

```python
# Storing a number
age = 30

# Storing text (called a string)
name = "Chris Idakwo"
date_of_birth = "2025/08/01"

# Storing a decimal number
height = 1.75

# Storing True or False (called boolean)
is_student = True
```

**Key Points:**
- The `=` sign is called the **assignment operator** - it assigns a value to a variable
- Text must be wrapped in quotes (single `'` or double `"` quotes)
- Numbers don't need quotes
- Variable names should be descriptive (use `student_age` instead of `x`)

**Changing Variable Values**

Variables are called "variable" because their values can change! You can update a variable by assigning it a new value.

```python
age = 30
print("Original age:", age)  # Prints: Original age: 30

# Update the age
age = 15
print("Updated age:", age)  # Prints: Updated age: 15
```

**Variable Naming Rules:**
1. Must start with a letter or underscore `_`
2. Can contain letters, numbers, and underscores
3. Cannot use spaces (use `student_name` not `student name`)
4. Cannot use Python reserved words (like `if`, `for`, `while`, etc.)
5. Use lowercase with underscores for multiple words (snake_case)

**Good Variable Names:**
```python
student_name = "John"
total_score = 95
is_passed = True
```

**Bad Variable Names:**
```python
# Don't start with a number
# 2name = "John"  # This will cause an error!

# Don't use spaces
# student name = "John"  # This will cause an error!

# Don't use reserved words
# if = 5  # This will cause an error!
```

**Printing Variables**

Use the `print()` function to display variable values:

```python
age = 30
name = "Chris"
print("Name:", name)
print("Age:", age)
```

**Output:**
```
Name: Chris
Age: 30
```

---

### Numbers

**Understanding Number Types**

Python has two main types of numbers:

1. **Integers (int)** - Whole numbers (no decimal points)
2. **Floats (float)** - Decimal numbers (numbers with decimal points)

**Integers**

Integers are whole numbers - they can be positive, negative, or zero.

```python
# Positive integers
age = 25
score = 100
count = 0

# Negative integers
temperature = -5
debt = -1000

# Large integers
population = 590870
big_number = -94858947584754394033
```

**Floats**

Floats are decimal numbers - they represent numbers with fractional parts.

```python
# Positive floats
height = 1.75
weight = 68.5
price = 99.99

# Negative floats
temperature = -3.5
balance = -45.67

# Even whole numbers can be floats if written with a decimal point
number = 12.0  # This is a float, not an integer!
```

**Checking Data Types**

You can check what type of data a variable contains using the `type()` function:

```python
age = 25
height = 1.75

print(type(age))    # Output: <class 'int'>
print(type(height)) # Output: <class 'float'>
```

**Why This Matters:**

Understanding the difference between integers and floats is important because:
- Some operations behave differently with each type
- Division always returns a float in Python (even if the result is a whole number)
- You might need to convert between types for certain operations

**Type Conversion**

You can convert between number types:

```python
# Convert integer to float
age = 25
age_float = float(age)
print(age_float)        # Output: 25.0
print(type(age_float))  # Output: <class 'float'>

# Convert float to integer (this truncates/removes the decimal part)
height = 1.75
height_int = int(height)
print(height_int)       # Output: 1 (note: it doesn't round, it truncates!)
```

**Important Note:** When converting a float to an integer, Python **truncates** (cuts off) the decimal part - it does NOT round. So `int(1.9)` becomes `1`, not `2`.

---

### Strings

**What are Strings?**

Strings are sequences of characters - basically, any text. They can contain letters, numbers, spaces, and special characters. In Python, strings are created by wrapping text in quotes.

```python
# Single quotes
name = 'Chris Idakwo'

# Double quotes
country = "Nigeria"

# Both work the same way!
greeting = "Hello"
greeting2 = 'Hello'  # Same as above
```

**String Length**

You can find out how many characters are in a string using the `len()` function:

```python
state = "Kaduna"
print(len(state))  # Output: 6 (K-a-d-u-n-a = 6 characters)

country = "Nigeria"
print(len(country))  # Output: 7
```

**String Methods - Changing Case**

Python provides methods to change the case of strings:

```python
country = "Nigeria"

# Convert to lowercase
print(country.lower())  # Output: "nigeria"

# Convert to uppercase
print(country.upper())  # Output: "NIGERIA"

# Convert to title case (first letter of each word capitalized)
event_name = "uefa champions league"
print(event_name.title())  # Output: "Uefa Champions League"
```

**Important:** These methods return a NEW string - they don't change the original string unless you reassign it:

```python
text = "Hello"
text.lower()  # This creates a new string but doesn't change 'text'
print(text)   # Still prints: "Hello"

# To actually change it, you need to reassign:
text = text.lower()
print(text)   # Now prints: "hello"
```

**String Checks**

You can check if a string contains only numbers using `.isnumeric()`:

```python
age = "9089"
print(age.isnumeric())  # Output: True

age2 = "90abc"
print(age2.isnumeric())  # Output: False (contains letters)
```

**Type Conversion with Strings**

You can convert numbers to strings and vice versa:

```python
# Convert number to string
age = 45
age_string = str(age)
print(age_string)        # Output: "45"
print(type(age_string)) # Output: <class 'str'>

# Convert string to number (if it contains only numbers)
age_text = "25"
age_number = int(age_text)
print(age_number)        # Output: 25
print(type(age_number)) # Output: <class 'int'>

# Convert string to float
price_text = "99.99"
price = float(price_text)
print(price)  # Output: 99.99
```

**String Slicing**

Slicing lets you extract parts of a string. The syntax is: `string[start:end:step]`

```python
greeting = "Hello, good morning"

# Get the full string
print(greeting[:])  # Output: "Hello, good morning"

# Get characters from index 0 to 5 (end index is exclusive)
print(greeting[0:5])  # Output: "Hello"

# Get characters from index 7 to the end
print(greeting[7:])   # Output: "good morning"

# Get characters from start to index 5
print(greeting[:5])   # Output: "Hello"

# Reverse a string using negative step
print(greeting[::-1])  # Output: "gninrom doog ,olleH"
```

**Understanding String Indexing:**

Strings are indexed starting from 0:
```
H  e  l  l  o
0  1  2  3  4
```

So `greeting[0]` is "H", `greeting[1]` is "e", etc.

**String Stripping**

Often, strings have unwanted spaces at the beginning or end. You can remove them:

```python
username = "  chris.idakwo@email.com  "

# Remove spaces from both sides
print(username.strip())   # Output: "chris.idakwo@email.com"

# Remove spaces from left side only
print(username.lstrip())  # Output: "chris.idakwo@email.com  "

# Remove spaces from right side only
print(username.rstrip())  # Output: "  chris.idakwo@email.com"

# You can also strip specific characters
email = "-/user@gmail.com&-"
print(email.strip("-&/"))  # Output: "user@gmail.com"
```

**String Concatenation**

Concatenation means joining strings together:

```python
first_name = "John"
last_name = "Doe"

# Using the + operator
full_name = first_name + " " + last_name
print(full_name)  # Output: "John Doe"

# When mixing strings and numbers, convert numbers to strings first
score = 80
sentence = first_name + " " + last_name + " scored " + str(score) + " out of 100"
print(sentence)  # Output: "John Doe scored 80 out of 100"
```

**String Formatting (F-Strings)**

F-strings (formatted string literals) make it easier to combine strings and variables:

```python
first_name = "John"
last_name = "Doe"
score = 80

# Using f-string (the 'f' before the quotes is important!)
sentence = f"{first_name} {last_name} scored {score} out of 100"
print(sentence)  # Output: "John Doe scored 80 out of 100"

# You can also do calculations inside f-strings
percentage = 85.5
print(f"The percentage is {percentage:.1f}%")  # Output: "The percentage is 85.5%"
```

**Alternative String Formatting**

You can also use the `.format()` method:

```python
first_name = "John"
last_name = "Doe"
score = 80

sentence = "{fname} {lname} scored {sc} out of 100".format(
    fname=first_name, 
    lname=last_name, 
    sc=score
)
print(sentence)  # Output: "John Doe scored 80 out of 100"
```

**F-strings are generally preferred** because they're easier to read and write!

---

### Math Operations

**Basic Arithmetic Operations**

Python supports all the standard math operations you learned in school:

**Addition (+)**

```python
print(1 + 5)    # Output: 6
print(-5 + 7)   # Output: 2
print(-28 + 7)  # Output: -21
```

**Subtraction (-)**

```python
print(4 - 5)    # Output: -1
print(-1 - 8)   # Output: -9
print(84 - 29)  # Output: 55
```

**Multiplication (*)**

```python
print(2 * 2)        # Output: 4
print(10 * 5)       # Output: 50
print(3.14 * 2)     # Output: 6.28
print(-2 * -8)      # Output: 16 (negative times negative = positive)
```

**Division (/)**

```python
print(4 / 2)        # Output: 2.0 (always returns a float!)
print(98.45 / 3.75) # Output: 26.253333333333332
print(-45 / 5)      # Output: -9.0
```

**Important:** Division in Python **always returns a float**, even if the result is a whole number. So `4 / 2` gives `2.0`, not `2`.

**Exponentiation (**)**

Exponentiation means raising a number to a power (multiplying a number by itself a certain number of times):

```python
print(2 ** 3)   # Output: 8 (2 * 2 * 2 = 8)
print(4 ** 3)   # Output: 64 (4 * 4 * 4 = 64)
print(5 ** 2)   # Output: 25 (5 * 5 = 25)
```

**Modulus (%)**

Modulus returns the remainder after division:

```python
print(3 % 2)    # Output: 1 (3 divided by 2 = 1 remainder 1)
print(10 % 3)   # Output: 1 (10 divided by 3 = 3 remainder 1)
print(8 % 4)    # Output: 0 (8 divided by 4 = 2 remainder 0)
```

**Modulus is useful for:**
- Checking if a number is even or odd (`num % 2 == 0` means even)
- Finding if a number is divisible by another
- Creating repeating patterns

**Order of Operations (BODMAS)**

Python follows the standard mathematical order of operations (BODMAS):
- **B**rackets
- **O**rders (exponents)
- **D**ivision
- **M**ultiplication
- **A**ddition
- **S**ubtraction

```python
print(4 + 6 - 2 / 4)      # Output: 9.5
# Step by step: 2/4 = 0.5, then 4 + 6 - 0.5 = 9.5

print(4 + (6 - 2) / 4)    # Output: 5.0
# Step by step: (6-2) = 4, then 4/4 = 1.0, then 4 + 1.0 = 5.0
```

**Using Parentheses**

Parentheses change the order of operations - operations inside parentheses are done first:

```python
result1 = 2 + 3 * 4      # Output: 14 (multiplication first: 3*4=12, then 2+12=14)
result2 = (2 + 3) * 4    # Output: 20 (parentheses first: 2+3=5, then 5*4=20)
```

**Math with Variables**

You can perform operations with variables:

```python
a = 10
b = 5

sum_result = a + b           # 15
difference = a - b            # 5
product = a * b               # 50
quotient = a / b              # 2.0
power = a ** b                # 100000
remainder = a % b             # 0

print(f"{a} + {b} = {sum_result}")
```

---

### User Input

**Getting Input from Users**

The `input()` function allows your program to get information from the user while it's running. The program will pause and wait for the user to type something and press Enter.

**Basic Input**

```python
name = input("What is your name? ")
print(f"Hello, {name}!")
```

When you run this, the program will:
1. Display "What is your name? " and wait
2. User types their name and presses Enter
3. The program continues and prints the greeting

**Important:** `input()` **always returns a string**, even if the user types a number!

```python
age = input("How old are you? ")
print(type(age))  # Output: <class 'str'> (it's a string, not a number!)
```

**Converting Input to Numbers**

Since `input()` returns a string, you need to convert it if you want to do math:

```python
# This will cause an error if you try to do math:
score = input("What was your score? ")
# score + 10  # ERROR! Can't add number to string

# Convert to number first:
score = float(input("What was your score? "))
percentage = (score / 100) * 10
print(f"Percentage: {percentage}")
```

**Type Conversion for Input:**

```python
# Convert to integer
age = int(input("Enter your age: "))

# Convert to float
height = float(input("Enter your height in meters: "))

# Keep as string (no conversion needed)
name = input("Enter your name: ")
```

**Method Chaining**

You can chain methods together to process input immediately:

```python
# Get input, strip whitespace, and convert to lowercase all at once
email = input("Enter your email: ").strip().lower()
print(email)

# Get input, strip, and replace text
email_address = input("Enter your email address: ").strip().replace("email", "outlook")
print(email_address)
```

**Multiple Inputs**

You can get multiple pieces of information:

```python
first_name = input("What is your first name? ")
last_name = input("What is your last name? ")
score = float(input("What was your score? "))

message = f"{first_name} {last_name} scored {score} out of 100"
print(message)
```

**Input Validation**

It's good practice to validate user input. We'll cover this more in the Control Flows section, but here's a simple example:

```python
score = input("Enter your score (0-100): ")
score_num = float(score)

if score_num < 0 or score_num > 100:
    print("Invalid score! Must be between 0 and 100")
else:
    print(f"Your score is {score_num}")
```

---

## Week 4 - Control Flows

### Comparison Operators

**What are Comparison Operators?**

Comparison operators compare two values and return `True` or `False`. They're used to make decisions in your code.

**Important Distinction:**
- `=` is the **assignment operator** (assigns a value)
- `==` is the **comparison operator** (checks if values are equal)

**Equal To (==)**

Checks if two values are equal:

```python
print(5 == 5)   # Output: True
print(5 == 3)   # Output: False
print("hello" == "hello")  # Output: True
print("hello" == "world")  # Output: False
```

**Not Equal To (!=)**

Checks if two values are NOT equal:

```python
print(5 != 5)   # Output: False
print(5 != 3)   # Output: True
print("apple" != "orange")  # Output: True
```

**Greater Than (>)**

Checks if the left value is greater than the right value:

```python
print(7 > 10)   # Output: False
print(10 > 7)   # Output: True
print(5 > 5)    # Output: False (5 is not greater than 5, it's equal)
```

**Less Than (<)**

Checks if the left value is less than the right value:

```python
print(7 < 10)   # Output: True
print(10 < 7)   # Output: False
print(5 < 5)    # Output: False
```

**Greater Than or Equal To (>=)**

Checks if the left value is greater than OR equal to the right value:

```python
print(7 >= 10)  # Output: False
print(10 >= 7)  # Output: True
print(5 >= 5)   # Output: True (5 is equal to 5, so it's True)
```

**Less Than or Equal To (<=)**

Checks if the left value is less than OR equal to the right value:

```python
print(7 <= 10)  # Output: True
print(10 <= 7)  # Output: False
print(5 <= 5)   # Output: True
```

**Using Comparison Operators with Variables**

```python
age = 25
minimum_age = 18

can_vote = age >= minimum_age
print(can_vote)  # Output: True

score = 85
passing_score = 60
passed = score >= passing_score
print(passed)  # Output: True
```

**Common Mistakes:**

```python
# WRONG - using = instead of ==
# if age = 18:  # This is assignment, not comparison! Error!

# CORRECT - using == for comparison
if age == 18:
    print("You are 18")
```

---

### Logical Operators

**What are Logical Operators?**

Logical operators combine or modify boolean (True/False) expressions. They let you create more complex conditions.

**AND Operator (and)**

The `and` operator returns `True` only if **ALL** conditions are `True`:

```python
age = 25
has_id = True

# Both conditions must be True
if age >= 18 and has_id:
    print("Give access!")  # This will print because both are True

# If any condition is False, the result is False
age = 15
if age >= 18 and has_id:
    print("Give access!")  # This won't print because age >= 18 is False
```

**Truth Table for AND:**
```
True and True   = True
True and False  = False
False and True  = False
False and False = False
```

**OR Operator (or)**

The `or` operator returns `True` if **AT LEAST ONE** condition is `True`:

```python
age = 25
has_id = False

# Only one condition needs to be True
if age >= 18 or has_id:
    print("Give access!")  # This will print because age >= 18 is True

# Both False = False
age = 15
has_id = False
if age >= 18 or has_id:
    print("Give access!")  # This won't print because both are False
```

**Truth Table for OR:**
```
True or True   = True
True or False  = True
False or True  = True
False or False = False
```

**NOT Operator (not)**

The `not` operator reverses/negates a boolean value:

```python
logged_in = False

if not logged_in:
    print("You're a guest")  # This will print because not False = True

logged_in = True
if not logged_in:
    print("You're a guest")  # This won't print because not True = False
```

**Truth Table for NOT:**
```
not True  = False
not False = True
```

**Combining Logical Operators**

You can combine multiple logical operators:

```python
age = 65
is_student = False

# Senior discount OR student discount
if age >= 60 or is_student:
    print("Yay, discount applied!")

# Must be adult AND have ID
age = 25
has_id = True
if age >= 18 and has_id:
    print("Access granted")

# Complex condition
temperature = 35
humidity = 15
if temperature > 30 or humidity < 20:
    print("Warning: Unusual weather condition!")
```

**Order of Evaluation:**

Python evaluates logical operators in this order:
1. `not` (highest priority)
2. `and`
3. `or` (lowest priority)

Use parentheses to make it clear:

```python
# Without parentheses (might be confusing)
if age >= 18 and has_id or is_vip:
    # This is evaluated as: (age >= 18 and has_id) or is_vip

# With parentheses (clearer)
if (age >= 18 and has_id) or is_vip:
    # Much clearer what you mean!
```

---

### If/Else Statements

**What are If/Else Statements?**

If/else statements let your program make decisions. They execute different code based on whether conditions are True or False.

**Basic If Statement**

```python
age = 20

if age >= 18:
    print("You are an adult")
```

**If-Else Statement**

```python
age = 15

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

**If-Elif-Else Statement**

Use `elif` (short for "else if") when you have multiple conditions:

```python
score = 85

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```

**Important Syntax Rules:**
1. Always end the condition with a colon `:`
2. Code inside the if/elif/else block must be indented (usually 4 spaces)
3. Python uses indentation to know what code belongs to which block

**Traffic Light Example:**

```python
light = input("What color is the traffic light? ").lower()

if light == "green" or light == "blinking":
    print("Go")
elif light == "yellow":
    print("Slow down")
else:
    print("Stop")
```

**Nested If Statements**

You can put if statements inside other if statements:

```python
age = 25
has_license = True

if age >= 18:
    if has_license:
        print("You can drive")
    else:
        print("You need a license")
else:
    print("You're too young to drive")
```

**Multiple Conditions:**

```python
temperature = 15
humidity = 15

if temperature > 30 or humidity < 20:
    print("Warning: Unusual weather condition detected!")
else:
    print("Weather conditions are normal")
```

**Common Patterns:**

**Pattern 1: Range Checking**
```python
score = 85

if 90 <= score <= 100:
    print("Excellent!")
elif 80 <= score < 90:
    print("Good!")
elif 70 <= score < 80:
    print("Average")
else:
    print("Needs improvement")
```

**Pattern 2: Input Validation**
```python
light = input("What color is the traffic light? ").lower()

allowed_colors = ["red", "yellow", "green", "blinking"]
if light in allowed_colors:
    if light == "green" or light == "blinking":
        print("Go")
    elif light == "yellow":
        print("Slow down")
    else:
        print("Stop")
else:
    print("Valid colors are red, green, yellow, and blinking ONLY!")
```

---

### Input Validation

**What is Input Validation?**

Input validation ensures that user input meets certain criteria before your program processes it. This prevents errors and makes your program more robust.

**Why Validate Input?**

- Users might type incorrect data
- Your program might crash with invalid input
- You want to provide helpful error messages

**Basic Validation Example:**

```python
light = input("What color is the traffic light? ").lower()

# Check if input is in allowed list
allowed_colors = ["red", "yellow", "green", "blinking"]

if light in allowed_colors:
    # Process valid input
    if light == "green" or light == "blinking":
        print("Go")
    elif light == "yellow":
        print("Slow down")
    else:
        print("Stop")
else:
    # Handle invalid input
    print("Valid colors are red, green, yellow, and blinking ONLY!")
```

**The `in` Operator**

The `in` operator checks if a value exists in a list:

```python
allowed_colors = ["red", "yellow", "green"]
color = "red"

if color in allowed_colors:
    print("Valid color!")
else:
    print("Invalid color!")
```

**Validating Numeric Input**

```python
# Get score and validate it's between 0 and 100
student_score = float(input("Enter score (0-100): "))

if student_score < 0 or student_score > 100:
    print("Invalid score! Please enter a score between 0 and 100")
else:
    print(f"Your score is {student_score}")
```

**Using While Loops for Validation**

You can keep asking until you get valid input (we'll cover while loops in detail later):

```python
student_score = float(input("Enter score (0-100): "))

# Keep asking until valid input
while student_score < 0 or student_score > 100:
    print("Invalid score! Please enter a score between 0 and 100")
    student_score = float(input("Enter score (0-100): "))

print(f"Thank you! Your score is {student_score}")
```

**Checking String Properties**

```python
age_text = input("Enter your age: ")

# Check if input is numeric
if age_text.isnumeric():
    age = int(age_text)
    print(f"You are {age} years old")
else:
    print("Please enter a valid number!")
```

**Multiple Validation Checks**

```python
age_text = input("Enter your age: ")

# Check multiple conditions
if age_text.isnumeric():
    age = int(age_text)
    if age >= 0 and age <= 120:
        print(f"You are {age} years old")
    else:
        print("Please enter a realistic age!")
else:
    print("Please enter a valid number!")
```

---

## Week 4 - Lists

### List Introduction

**What are Lists?**

Lists are containers that hold multiple values in a single variable. Think of them like a shopping list, a playlist, or a row of boxes - they keep related items together in order.

**Creating Lists**

Lists are created using square brackets `[]`:

```python
# List of numbers
scores = [56, 90, 34, 75, 45, 89, 65, 45]

# List of strings
shopping = ["rice", "milk", "bread", "eggs", "butter"]

# List of mixed types (not recommended, but possible)
mixed = ["John", 25, False, 3.14, ["Chris"]]

# Empty list (you can add items later)
empty_list = []
```

**Key Characteristics:**
- **Ordered**: Items have a specific order (first item, second item, etc.)
- **Mutable**: You can change, add, or remove items
- **Can contain duplicates**: Same value can appear multiple times
- **Indexed**: Each item has a position number (starting from 0)

**List Length**

Find how many items are in a list using `len()`:

```python
ages = [25, 30, 46, 94, 13, 24]
list_length = len(ages)
print("Number of items:", list_length)  # Output: 6
```

**Lists are Mutable**

Unlike strings (which are immutable), you can change lists:

```python
shopping = ["rice", "milk", "bread"]

# Add an item
shopping.append("eggs")  # Adds "eggs" to the end
print(shopping)  # Output: ["rice", "milk", "bread", "eggs"]

# Change an item
shopping[0] = "wheat"  # Changes first item
print(shopping)  # Output: ["wheat", "milk", "bread", "eggs"]

# Remove an item
shopping.remove("milk")  # Removes "milk"
print(shopping)  # Output: ["wheat", "bread", "eggs"]
```

**Common List Operations:**

```python
fruits = ["apple", "banana"]

# Add to end
fruits.append("orange")  # ["apple", "banana", "orange"]

# Insert at specific position
fruits.insert(1, "grape")  # ["apple", "grape", "banana", "orange"]

# Remove by value
fruits.remove("banana")  # ["apple", "grape", "orange"]

# Remove by index
fruits.pop(0)  # Removes and returns "apple"
```

**Lists from User Input**

You can create lists from user input:

```python
student_name = input("Enter student name: ")
student_age = int(input("Enter student age: "))
student_grade = input("Enter student grade: ")

student_info = [student_name, student_age, student_grade]
print("Student information:", student_info)
```

---

### Accessing List Items

**Understanding List Indexing**

Lists are **zero-indexed**, meaning the first item is at position 0, not 1:

```python
names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah"]

# Index positions:
# "Mike"     = index 0
# "Jane"     = index 1
# "Blessing" = index 2
# "Peter"    = index 3
# "Joe"      = index 4
# "Sarah"    = index 5
```

**Accessing Items by Index**

Use square brackets with the index number:

```python
names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah"]

print(names[0])   # Output: "Mike" (first item)
print(names[1])   # Output: "Jane" (second item)
print(names[2])   # Output: "Blessing" (third item)
print(names[5])   # Output: "Sarah" (last item)
```

**Negative Indexing**

Python allows negative indexing to count from the end:

```python
names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah"]

print(names[-1])  # Output: "Sarah" (last item)
print(names[-2])  # Output: "Joe" (second to last)
print(names[-3])  # Output: "Peter" (third from last)
```

**Negative Index Positions:**
```
"Mike"     = index -6
"Jane"     = index -5
"Blessing" = index -4
"Peter"    = index -3
"Joe"      = index -2
"Sarah"    = index -1
```

**Getting the Last Item**

Two ways to get the last item:

```python
names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah"]

# Method 1: Negative indexing (easier!)
last_item = names[-1]

# Method 2: Using length
last_item = names[len(names) - 1]

print(last_item)  # Output: "Sarah"
```

**IndexError**

If you try to access an index that doesn't exist, you'll get an error:

```python
names = ["Mike", "Jane", "Blessing"]

# This will cause an error because index 9 doesn't exist
# print(names[9])  # IndexError: list index out of range
```

**Changing List Items**

You can change items by assigning a new value to an index:

```python
names = ["Mike", "Jane", "Blessing"]
names[0] = "Michael"  # Changes "Mike" to "Michael"
print(names)  # Output: ["Michael", "Jane", "Blessing"]
```

---

### List Slicing

**What is Slicing?**

Slicing extracts a portion (a "slice") of a list. It's like cutting a piece of cake - you get a specific part of the whole.

**Slicing Syntax**

The syntax is: `list[start:end:step]`
- `start`: Index where slicing begins (inclusive)
- `end`: Index where slicing ends (exclusive - not included!)
- `step`: How many items to skip (optional)

**Basic Slicing**

```python
names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah", "Chris", "Daniel"]

# Get items from index 2 to 6 (end index is exclusive!)
print(names[2:6])  # Output: ["Blessing", "Peter", "Joe", "Sarah"]
# Note: Gets indices 2, 3, 4, 5 (stops before 6)

# Get all items
print(names[:])  # Output: Full list

# Get items from start to index 4
print(names[:4])  # Output: ["Mike", "Jane", "Blessing", "Peter"]

# Get items from index 2 to end
print(names[2:])  # Output: ["Blessing", "Peter", "Joe", "Sarah", "Chris", "Daniel"]
```

**Important:** The end index is **exclusive** - it's not included in the result!

**Step Slicing**

The step parameter lets you skip items:

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# Get every 2nd item (step of 2)
print(numbers[::2])  # Output: [0, 2, 4, 6, 8]

# Get every 3rd item
print(numbers[::3])  # Output: [0, 3, 6, 9]

# Reverse a list
print(numbers[::-1])  # Output: [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
```

**Common Slicing Patterns:**

```python
my_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# First 3 items
print(my_list[:3])  # [0, 1, 2]

# Last 3 items
print(my_list[-3:])  # [7, 8, 9]

# Middle items (indices 2 to 7)
print(my_list[2:8])  # [2, 3, 4, 5, 6, 7]

# Every other item
print(my_list[::2])  # [0, 2, 4, 6, 8]

# Reverse
print(my_list[::-1])  # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
```

---

### List Operations

**Common List Methods**

Python provides many useful methods for working with lists:

**Adding Items**

```python
fruits = ["apple", "banana"]

# append() - Add to end
fruits.append("orange")  # ["apple", "banana", "orange"]

# insert() - Add at specific position
fruits.insert(1, "grape")  # ["apple", "grape", "banana", "orange"]
```

**Removing Items**

```python
fruits = ["apple", "banana", "orange", "apple"]

# remove() - Remove first occurrence of value
fruits.remove("apple")  # ["banana", "orange", "apple"]

# pop() - Remove and return item at index (default: last item)
last_fruit = fruits.pop()  # Removes and returns "apple"
first_fruit = fruits.pop(0)  # Removes and returns "banana"
```

**Finding Items**

```python
fruits = ["apple", "banana", "orange"]

# Check if item exists
if "apple" in fruits:
    print("Apple is in the list")

# Find index of item
index = fruits.index("banana")  # Returns 1
```

**Other Useful Operations**

```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6]

# Count occurrences
count = numbers.count(1)  # Returns 2

# Sort (modifies original list)
numbers.sort()  # [1, 1, 2, 3, 4, 5, 6, 9]

# Reverse
numbers.reverse()  # [9, 6, 5, 4, 3, 2, 1, 1]

# Clear all items
numbers.clear()  # []
```

---

## Week 4 - Loops

### For Loops

**What are For Loops?**

For loops repeat code a specific number of times. They iterate (go through) each item in a sequence (like a string, list, or range of numbers).

**Basic For Loop Syntax**

```python
for item in sequence:
    # Code to execute for each item
    print(item)
```

**Iterating Over a String**

```python
name = "Chris Idakwo"
for char in name:
    print(char)
```

**Output:**
```
C
h
r
i
s
 
I
d
a
k
w
o
```

**Iterating Over a List**

```python
names = ["Mike", "Jane", "Blessing"]
for name in names:
    print(f"Hello, {name}!")
```

**Output:**
```
Hello, Mike!
Hello, Jane!
Hello, Blessing!
```

**Using range()**

The `range()` function creates a sequence of numbers:

```python
# range(stop) - from 0 to stop-1
for num in range(5):
    print(num)  # Prints: 0, 1, 2, 3, 4

# range(start, stop) - from start to stop-1
for num in range(1, 6):
    print(num)  # Prints: 1, 2, 3, 4, 5

# range(start, stop, step) - with step
for num in range(0, 10, 2):
    print(num)  # Prints: 0, 2, 4, 6, 8
```

**Common range() Patterns:**

```python
# Count from 1 to 10
for i in range(1, 11):
    print(i)

# Count backwards
for i in range(10, 0, -1):
    print(i)  # Prints: 10, 9, 8, 7, 6, 5, 4, 3, 2, 1

# Count by 5s
for i in range(0, 50, 5):
    print(i)  # Prints: 0, 5, 10, 15, 20, 25, 30, 35, 40, 45
```

**Using enumerate() for Index and Value**

Sometimes you need both the index and the value:

```python
names = ["Mike", "Jane", "Blessing"]

for index, name in enumerate(names):
    print(f"{index}: {name}")
```

**Output:**
```
0: Mike
1: Jane
2: Blessing
```

**Practical Examples:**

```python
# Sum numbers in a list
numbers = [1, 2, 3, 4, 5]
total = 0
for num in numbers:
    total = total + num
print(f"Sum: {total}")  # Output: Sum: 15

# Find maximum value
scores = [85, 92, 78, 96, 88]
max_score = scores[0]
for score in scores:
    if score > max_score:
        max_score = score
print(f"Highest score: {max_score}")  # Output: Highest score: 96
```

---

### While Loops

**What are While Loops?**

While loops repeat code as long as a condition is `True`. Unlike for loops (which run a specific number of times), while loops run until a condition becomes `False`.

**Basic While Loop Syntax**

```python
while condition:
    # Code to execute while condition is True
    print("Looping...")
```

**Simple Counter Example**

```python
count = 1
while count <= 20:
    print(count)
    count = count + 1  # Important: update the counter!

print("I'm outside the while loop")
```

**Output:**
```
1
2
3
...
20
I'm outside the while loop
```

**Important:** You must update the variable in the condition, or the loop will run forever (infinite loop)!

**Flag-Controlled Loop**

Use a flag (boolean variable) to control the loop:

```python
found = False
attempts = 0

while not found and attempts < 5:
    guess = input("Guess the number: ")
    if guess == "42":
        found = True
        print("Correct!")
    else:
        attempts = attempts + 1
        print("Try again!")
```

**Input Validation with While Loop**

Keep asking until you get valid input:

```python
student_score = float(input("Enter score (0-100): "))

while student_score < 0 or student_score > 100:
    print("Invalid score! Please enter a score between 0 and 100")
    student_score = float(input("Enter score (0-100): "))

print(f"Thank you! Your score is {student_score}")
```

**Infinite Loops (and how to avoid them)**

An infinite loop runs forever because the condition never becomes False:

```python
# DANGER: Infinite loop!
# count = 1
# while count <= 10:
#     print(count)
#     # Forgot to increment count! This will run forever!

# CORRECT: Update the counter
count = 1
while count <= 10:
    print(count)
    count = count + 1  # This prevents infinite loop
```

**Common While Loop Patterns:**

**Pattern 1: Counter**
```python
count = 0
while count < 5:
    print(f"Count: {count}")
    count += 1
```

**Pattern 2: User Input Validation**
```python
valid = False
while not valid:
    age = input("Enter your age: ")
    if age.isnumeric():
        valid = True
    else:
        print("Please enter a number!")
```

**Pattern 3: Menu System**
```python
choice = ""
while choice != "quit":
    print("1. Option 1")
    print("2. Option 2")
    print("Type 'quit' to exit")
    choice = input("Enter choice: ")
```

---

### Break Statement

**What is Break?**

The `break` statement immediately exits the loop when encountered, even if the loop condition is still `True`.

**Basic Break Example**

```python
for num in range(1, 1001):
    guess = int(input("Guess the number: "))
    if guess == 42:
        print("Correct! You've found the number 42")
        break  # Exit the loop immediately
    print("Try again!")
```

**Without Break (Inefficient):**

```python
found = False
for num in range(1, 1001):
    if not found:
        guess = int(input("Guess the number: "))
        if guess == 42:
            found = True
            print("Correct!")
    if not found:
        print("Try again!")
```

**With Break (Better):**

```python
for num in range(1, 1001):
    guess = int(input("Guess the number: "))
    if guess == 42:
        print("Correct!")
        break  # Much cleaner!
    print("Try again!")
```

**Break with Condition**

```python
# Print even numbers up to 20
for num in range(1, 1001):
    if num > 20:
        break  # Exit when num exceeds 20
    if num % 2 == 0:
        print(num)
```

**Break in While Loops**

```python
count = 1
while True:  # Infinite loop
    print(count)
    count += 1
    if count > 10:
        break  # Exit the loop
```

**When to Use Break:**

- When you find what you're looking for and don't need to continue
- When an error condition occurs
- When user wants to exit early
- To avoid unnecessary iterations

---

### Continue Statement

**What is Continue?**

The `continue` statement skips the rest of the current iteration and moves to the next one. It doesn't exit the loop - it just skips ahead.

**Basic Continue Example**

```python
# Print only odd numbers (skip even numbers)
for num in range(1, 11):
    if num % 2 == 0:
        continue  # Skip this iteration, go to next number
    print(num)  # Only prints odd numbers
```

**Output:**
```
1
3
5
7
9
```

**What Happens:**

1. Loop starts with `num = 1`
2. `1 % 2 == 0` is `False`, so `continue` is NOT executed
3. `print(1)` executes
4. Loop continues with `num = 2`
5. `2 % 2 == 0` is `True`, so `continue` executes
6. `print(2)` is SKIPPED
7. Loop continues with `num = 3`
8. And so on...

**Continue vs Break:**

```python
# Using break - exits loop completely
for num in range(1, 11):
    if num == 5:
        break  # Loop stops here
    print(num)
# Output: 1, 2, 3, 4

# Using continue - skips current iteration
for num in range(1, 11):
    if num == 5:
        continue  # Skip 5, continue with 6
    print(num)
# Output: 1, 2, 3, 4, 6, 7, 8, 9, 10
```

**Practical Example:**

```python
# Process only valid scores
scores = [85, -5, 92, 0, 78, 150, 96]

for score in scores:
    if score < 0 or score > 100:
        continue  # Skip invalid scores
    print(f"Valid score: {score}")
```

**Output:**
```
Valid score: 85
Valid score: 92
Valid score: 0
Valid score: 78
Valid score: 96
```

**When to Use Continue:**

- To skip invalid data
- To skip certain conditions
- To make code more readable (avoid deep nesting)
- To process only specific items

---

## Week 5 - Dictionaries

### Dictionary Introduction

**What are Dictionaries?**

Dictionaries store data in **key-value pairs**. Think of them like a real dictionary: you look up a word (key) to find its definition (value). Or like a contact list: you look up a name (key) to find their phone number (value).

**Key Characteristics:**
- **Key-Value Pairs**: Each item has a key (like a label) and a value (the data)
- **Keys must be unique**: No duplicate keys allowed
- **Keys must be immutable**: Usually strings, numbers, or tuples
- **Values can be anything**: Strings, numbers, lists, other dictionaries, etc.
- **Ordered**: As of Python 3.7+, dictionaries maintain insertion order
- **Mutable**: You can add, change, or remove items

**Creating Dictionaries**

**Method 1: Dictionary Literal (Curly Braces)**

```python
student_a = {
    "first_name": "Chris",
    "last_name": "Idakwo",
    "age": 20,
    "height": 1.65,
    "gender": "Male",
    "registered": True,
    "skills": []
}
```

**Method 2: dict() Constructor**

```python
student_b = dict(
    first_name="Chris",
    last_name="Idakwo",
    age=20,
    height=1.65,
    gender="Male"
)
```

**Empty Dictionary**

```python
empty_dict = {}
# or
empty_dict = dict()
```

**Dictionary Structure:**

```python
person = {
    "name": "John",      # key: "name", value: "John"
    "age": 30,           # key: "age", value: 30
    "city": "Lagos"      # key: "city", value: "Lagos"
}
```

**Keys and Values:**

- **Keys**: The labels (left side) - must be unique strings
- **Values**: The data (right side) - can be any type

**Nested Dictionaries**

Dictionaries can contain other dictionaries:

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50,
    "pets": {
        "dog": "Frieda",
        "cat": "Sox"
    },
    "kids": ["Joe", "Martha", "Sarah"]
}
```

**Dictionaries are Mutable**

You can add, change, or remove items:

```python
student = {
    "name": "John",
    "age": 20
}

# Add new key-value pair
student["email"] = "john@example.com"

# Update existing value
student["age"] = 21

# Remove key-value pair
del student["age"]
```

---

### Accessing Dictionary Values

**Basic Access**

Access values using square brackets with the key name:

```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "engineLitre": 5.0,
    "transmission": "manual"
}

# Access single value
trans = car["transmission"]
print(trans)  # Output: "manual"

brand = car["brand"]
print(brand)  # Output: "Ford"
```

**KeyError**

If you try to access a key that doesn't exist, you'll get a KeyError:

```python
# This will cause an error:
# print(car["color"])  # KeyError: 'color'
```

**Accessing Nested Dictionaries**

When dictionaries contain other dictionaries, chain the square brackets:

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50,
    "pets": {
        "dog": "Frieda",
        "cat": "Sox"
    },
    "kids": ["Joe", "Martha", "Sarah"]
}

# Access nested dictionary
dog_name = person["pets"]["dog"]
print(dog_name)  # Output: "Frieda"

cat_name = person["pets"]["cat"]
print(cat_name)  # Output: "Sox"
```

**Accessing Lists Within Dictionaries**

If a dictionary value is a list, you can access list items:

```python
person = {
    "kids": ["Joe", "Martha", "Sarah"]
}

# Get the first child
first_child = person["kids"][0]
print(first_child)  # Output: "Joe"

# Get the second child
second_child = person["kids"][1]
print(second_child)  # Output: "Martha"
```

**Combining Nested Access**

You can combine nested dictionary and list access:

```python
person = {
    "pets": {"dog": "Frieda", "cat": "Sox"},
    "kids": ["Joe", "Martha", "Sarah"]
}

# Get second child
second_child = person["kids"][1]  # "Martha"

# Get dog name
dog_name = person["pets"]["dog"]  # "Frieda"
```

**Safe Access with get()**

The `.get()` method returns `None` (instead of error) if key doesn't exist:

```python
car = {"brand": "Ford", "model": "Mustang"}

# Using square brackets (causes error if key missing)
# color = car["color"]  # KeyError!

# Using get() (returns None if key missing)
color = car.get("color")  # Returns None, no error!
print(color)  # Output: None

# You can provide a default value
color = car.get("color", "Unknown")  # Returns "Unknown" if key missing
print(color)  # Output: "Unknown"
```

---

### Dictionary Methods

**Common Dictionary Methods**

Python provides many useful methods for working with dictionaries:

**get() Method**

Safely retrieve a value, with optional default:

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50
}

# Get existing key
first_name = person.get("first_name")  # "John"

# Get non-existent key (returns None)
middle_name = person.get("middle_name")  # None

# Get with default value
middle_name = person.get("middle_name", "N/A")  # "N/A"
```

**keys() Method**

Returns all keys in the dictionary:

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50
}

keys = person.keys()
print(keys)  # Output: dict_keys(['first_name', 'last_name', 'age'])

# Convert to list if needed
keys_list = list(person.keys())
print(keys_list)  # Output: ['first_name', 'last_name', 'age']
```

**values() Method**

Returns all values in the dictionary:

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50
}

values = person.values()
print(values)  # Output: dict_values(['John', 'Doe', 50])
```

**items() Method**

Returns key-value pairs as tuples:

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50
}

items = person.items()
print(items)  
# Output: dict_items([('first_name', 'John'), ('last_name', 'Doe'), ('age', 50)])

# Iterate over items
for key, value in person.items():
    print(f"{key}: {value}")
```

**Output:**
```
first_name: John
last_name: Doe
age: 50
```

**pop() Method**

Removes and returns the value for a given key:

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50
}

last_name = person.pop("last_name")
print(last_name)  # Output: "Doe"
print(person)     # Output: {'first_name': 'John', 'age': 50}
```

**copy() Method**

Creates a shallow copy of the dictionary:

```python
person = {
    "first_name": "John",
    "last_name": "Doe"
}

person_copy = person.copy()
person_copy["age"] = 30

print(person)      # {'first_name': 'John', 'last_name': 'Doe'}
print(person_copy) # {'first_name': 'John', 'last_name': 'Doe', 'age': 30}
```

**clear() Method**

Removes all items from the dictionary:

```python
person = {
    "first_name": "John",
    "last_name": "Doe"
}

person.clear()
print(person)  # Output: {}
```

**Using items() for Iteration**

The `items()` method is very useful for looping:

```python
library = {
    "The Hobbit": {
        "author": "J.R.R. Tolkien",
        "year": 1937,
        "genre": "Fantasy",
        "read": True
    },
    "Dune": {
        "author": "Frank Herbert",
        "year": 1965,
        "genre": "Fiction",
        "read": False
    }
}

for book_title, book_details in library.items():
    print(f"Book Title: {book_title}")
    print(f"Book Details: {book_details}")
    print("")
```

**Output:**
```
Book Title: The Hobbit
Book Details: {'author': 'J.R.R. Tolkien', 'year': 1937, 'genre': 'Fantasy', 'read': True}

Book Title: Dune
Book Details: {'author': 'Frank Herbert', 'year': 1965, 'genre': 'Fiction', 'read': False}
```

---

### Dictionary Operations

**Adding and Updating Items**

```python
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50
}

# Add new key-value pair
person["dob"] = "05/05/1975"
person["email"] = "john@example.com"

# Update existing value
person["age"] = 51

print(person)
```

**Checking if Key Exists**

Use the `in` operator:

```python
person = {
    "first_name": "John",
    "last_name": "Doe"
}

# Check if key exists
if "first_name" in person:
    print("Found the key: first_name")

if "gender" in person:
    print("Found the key: gender")
else:
    print("Could not find the key: gender")
```

**Iterating Over Dictionaries**

**Method 1: Iterate over keys**

```python
person = {"name": "John", "age": 30, "city": "Lagos"}

for key in person:
    print(f"{key}: {person[key]}")
```

**Method 2: Iterate over items (recommended)**

```python
person = {"name": "John", "age": 30, "city": "Lagos"}

for key, value in person.items():
    print(f"{key}: {value}")
```

**Method 3: Iterate over values only**

```python
person = {"name": "John", "age": 30, "city": "Lagos"}

for value in person.values():
    print(value)
```

**Nested Dictionary Operations**

Working with nested dictionaries:

```python
students = {
    "student1": {
        "name": "John",
        "age": 20,
        "grades": [85, 90, 88]
    },
    "student2": {
        "name": "Jane",
        "age": 21,
        "grades": [92, 95, 90]
    }
}

# Access nested data
john_name = students["student1"]["name"]
john_first_grade = students["student1"]["grades"][0]

# Update nested data
students["student1"]["age"] = 21

# Add to nested list
students["student1"]["grades"].append(95)
```

**Dictionary Comprehensions (Advanced)**

Create dictionaries using comprehensions:

```python
# Create dictionary from range
squared = {x: x**2 for x in range(5)}
print(squared)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

# Create from list
names = ["John", "Jane", "Bob"]
name_lengths = {name: len(name) for name in names}
print(name_lengths)  # Output: {'John': 4, 'Jane': 4, 'Bob': 3}
```

**Common Dictionary Patterns:**

**Pattern 1: Counting Occurrences**
```python
words = ["apple", "banana", "apple", "orange", "banana", "apple"]
count = {}

for word in words:
    if word in count:
        count[word] += 1
    else:
        count[word] = 1

print(count)  # Output: {'apple': 3, 'banana': 2, 'orange': 1}
```

**Pattern 2: Grouping Data**
```python
students = [
    {"name": "John", "grade": "A"},
    {"name": "Jane", "grade": "B"},
    {"name": "Bob", "grade": "A"}
]

by_grade = {}
for student in students:
    grade = student["grade"]
    if grade not in by_grade:
        by_grade[grade] = []
    by_grade[grade].append(student["name"])

print(by_grade)  # Output: {'A': ['John', 'Bob'], 'B': ['Jane']}
```

---

## Week 5 - Working with Files

### File Introduction

**What are Files?**

Files let you store data on disk and read or write it from your program. Python uses the built-in `open()` function to work with files.

**Opening and Closing Files**

```python
# Open for reading (default)
file = open("example.txt")
content = file.read()
file.close()

# Using with (recommended - auto-closes)
with open("example.txt") as f:
    content = f.read()
```

---

### Reading from Files

Use `.read()` for the whole file, `.readline()` for one line, or `.readlines()` for a list of lines.

```python
with open("greeting.txt") as f:
    content = f.read()   # Entire file as string
    # line = f.readline()   # One line
    # lines = f.readlines() # List of lines
```

---

### Reading File Lines

Iterate over the file object to process line by line without loading the whole file.

```python
with open("log.txt") as f:
    for line in f:
        print(line.strip())
```

---

### Writing to Files

Open with mode `'w'` to write (overwrites existing content). Use `.write()` or `.writelines()`.

```python
with open("output.txt", "w") as f:
    f.write("Hello, World!\n")
```

---

### Appending to Files

Open with mode `'a'` to add content without overwriting.

```python
with open("log.txt", "a") as f:
    f.write("New log entry\n")
```

---

### Processing CSV Data

The `csv` module helps read and write CSV files.

```python
import csv
with open("data.csv", newline='') as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

---

## Week 6 - Functions

### Function Introduction

**What are Functions?**

Functions are reusable blocks of code. You define them with `def`, then call them by name.

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Chris")  # Hello, Chris!
```

---

### Return Values

Use `return` to send a value back. Without `return`, the function returns `None`.

```python
def add(a, b):
    return a + b

result = add(3, 5)  # 8
```

---

### Default Parameters

Parameters can have default values so callers can omit them.

```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

print(greet("Chris"))        # Hello, Chris!
print(greet("Chris", "Hi"))  # Hi, Chris!
```

---

### Positional and Keyword Arguments

Arguments can be passed by position or by name (keyword).

```python
def describe(name, age, city="Lagos"):
    return f"{name}, {age}, from {city}"

describe("John", 30)
describe("John", 30, city="Abuja")
describe(age=25, name="Jane", city="Kano")
```

---

### Return Multiple Values

Functions can return multiple values as a tuple; callers can unpack them.

```python
def min_max(numbers):
    return min(numbers), max(numbers)

low, high = min_max([3, 1, 4, 1, 5])
```

---

### Variable Scope

Variables inside a function are local. Use `global` to modify a global variable from inside a function.

```python
count = 0

def increment():
    global count
    count += 1

increment()
print(count)  # 1
```

---

## Week 7 - Advanced Working with Files

### Reading from CSV Files

Use `csv.DictReader()` to get each row as a dictionary with headers as keys.

```python
import csv
with open("students_grades.csv", newline='') as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(row["name"], row["grade"])
```

---

### Writing to CSV Files

Use `csv.writer()` or `csv.DictWriter()` to write CSV data.

```python
import csv
with open("output.csv", "w", newline='') as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Score"])
    writer.writerows([["Alice", 95], ["Bob", 87]])
```

---

### CSV Quotes

The `csv` module handles quoting with `quoting` and `quotechar` for special characters in fields.

```python
import csv
with open("data.csv", "w", newline='') as f:
    writer = csv.writer(f, quoting=csv.QUOTE_MINIMAL)
    writer.writerow(["Name", "Description"])
```

---

### Working with OS Module

The `os` module provides path and environment operations: `os.getcwd()`, `os.listdir()`, `os.path.join()`, `os.path.exists()`, etc.

```python
import os
print(os.getcwd())
print(os.listdir("."))
path = os.path.join("folder", "file.txt")
if os.path.exists(path):
    print("File exists")
```

---

### Directory Utilities

Combine `os` and `os.path` to list directories and check file vs directory.

```python
import os
for name in os.listdir("files"):
    full_path = os.path.join("files", name)
    if os.path.isfile(full_path):
        print(f"File: {name}")
    elif os.path.isdir(full_path):
        print(f"Dir: {name}")
```

---

## Summary

This bootcamp has covered fundamental Python programming concepts:

### Week 3 - Python Basics
- **Variables**: Containers for storing data
- **Numbers**: Integers and floats
- **Strings**: Text manipulation and formatting
- **Math Operations**: Arithmetic, order of operations
- **User Input**: Getting and processing user data

### Week 4 - Control Flows
- **Comparison Operators**: Comparing values (`==`, `!=`, `>`, `<`, `>=`, `<=`)
- **Logical Operators**: Combining conditions (`and`, `or`, `not`)
- **If/Else Statements**: Making decisions in code
- **Input Validation**: Ensuring data meets requirements

### Week 4 - Lists
- **List Creation**: Storing multiple values
- **Accessing Items**: Using indices (positive and negative)
- **List Slicing**: Extracting portions of lists
- **List Operations**: Adding, removing, and modifying items

### Week 4 - Loops
- **For Loops**: Iterating over sequences
- **While Loops**: Repeating until condition is met
- **Break**: Exiting loops early
- **Continue**: Skipping iterations

### Week 5 - Dictionaries
- **Dictionary Creation**: Key-value pair storage
- **Accessing Values**: Retrieving data by key
- **Dictionary Methods**: Built-in operations
- **Dictionary Operations**: Adding, updating, iterating

### Week 5 - Working with Files
- **File Introduction**: Opening and closing files with `open()` and `with`
- **Reading from Files**: `.read()`, `.readline()`, `.readlines()`, iterating lines
- **Writing to Files**: Mode `'w'`, `.write()`, `.writelines()`
- **Appending to Files**: Mode `'a'`
- **Processing CSV Data**: `csv.reader()`, `csv.writer()`

### Week 6 - Functions
- **Function Introduction**: Defining with `def`, calling functions
- **Return Values**: Using `return`
- **Default Parameters**: Optional arguments with default values
- **Positional and Keyword Arguments**: Passing by position or name
- **Return Multiple Values**: Tuples and unpacking
- **Variable Scope**: Local vs global, `global` keyword

### Week 7 - Advanced Working with Files
- **Reading from CSV Files**: `csv.DictReader()` for rows as dictionaries
- **Writing to CSV Files**: `csv.writer()`, `csv.DictWriter()`
- **CSV Quotes**: Quoting options for special characters
- **Working with OS Module**: `os.getcwd()`, `os.listdir()`, `os.path.join()`, `os.path.exists()`
- **Directory Utilities**: Listing and checking files vs directories with `os.path.isfile()`, `os.path.isdir()`

### Key Concepts to Remember:

1. **Python is zero-indexed**: Lists and strings start counting at 0
2. **Indentation matters**: Python uses indentation to define code blocks
3. **Types matter**: Know when you're working with strings vs numbers
4. **Dictionaries are powerful**: Great for organizing related data
5. **Loops save time**: Use loops to avoid repeating code
6. **Validation is important**: Always check user input
7. **Use `with` for files**: Ensures files are closed properly
8. **Functions reduce repetition**: Define once, call many times

Happy coding! 🐍
