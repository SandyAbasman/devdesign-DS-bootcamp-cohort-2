# Python Learning Guide - Data Science Bootcamp Cohort 2

This document provides a comprehensive overview of all Python concepts taught in the bootcamp, along with JavaScript equivalents for each concept.

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

**Python Concept:**
Variables are containers that store data values. In Python, you don't need to declare a variable's type - it's inferred from the value assigned.

**Python Example:**
```python
age = 30
date_of_birth = "2025/08/01"
name = "Chris Idakwo"

# Variables can be reassigned
age = 15
print("The updated value of age is", age)
```

**JavaScript Equivalent:**
```javascript
let age = 30;
const dateOfBirth = "2025/08/01";
let name = "Chris Idakwo";

// Variables can be reassigned
age = 15;
console.log("The updated value of age is", age);
```

**Key Differences:**
- Python uses `=` for assignment, JavaScript uses `let`, `const`, or `var`
- Python doesn't require variable declaration keywords
- JavaScript has `const` for constants (Python doesn't have this distinction)
- Python uses `print()`, JavaScript uses `console.log()`

---

### Numbers

**Python Concept:**
Python has two main numeric types: integers (whole numbers) and floats (decimal numbers).

**Python Example:**
```python
# Integers
a = 10
b = 590870
c = -94858947584754394033

# Floats
f1 = 12.0
f2 = 93.8
f3 = -780.35

# Check data type
print(type(a))  # <class 'int'>
print(type(f1))  # <class 'float'>
```

**JavaScript Equivalent:**
```javascript
// JavaScript has only one number type (Number)
let a = 10;
let b = 590870;
let c = -94858947584754394033;

// Floats
let f1 = 12.0;
let f2 = 93.8;
let f3 = -780.35;

// Check data type
console.log(typeof a);  // "number"
console.log(typeof f1); // "number"
```

**Key Differences:**
- Python has separate `int` and `float` types
- JavaScript has a single `Number` type that handles both integers and floats
- Python uses `type()`, JavaScript uses `typeof`

---

### Strings

**Python Concept:**
Strings are sequences of characters. Python provides many built-in methods for string manipulation.

**Python Example:**
```python
state = "Kaduna"
country = "Nigeria"

# String length
print(len(state))  # 6

# Case conversion
print(country.lower())      # "nigeria"
print(country.upper())      # "NIGERIA"
print("uefa champions league".title())  # "Uefa Champions League"

# String checks
age = "9089"
print(age.isnumeric())  # True

# Type conversion
age = 45
print(str(age))  # "45"

# String slicing
greeting = "Hello, good morning"
print(greeting[:])        # Full string
print(greeting[::-1])     # Reversed: "gninrom doog ,olleH"

# String stripping
username = "  chris.idakwo@email.com  "
print(username.strip())   # "chris.idakwo@email.com"
print(username.lstrip())  # "chris.idakwo@email.com  "
print(username.rstrip())  # "  chris.idakwo@email.com"

# String concatenation
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name

# String formatting (f-strings)
score = 80
sentence = f"{first_name} {last_name} scored {score} out of 100"
```

**JavaScript Equivalent:**
```javascript
let state = "Kaduna";
let country = "Nigeria";

// String length
console.log(state.length);  // 6

// Case conversion
console.log(country.toLowerCase());      // "nigeria"
console.log(country.toUpperCase());     // "NIGERIA"
console.log("uefa champions league".replace(/\b\w/g, l => l.toUpperCase()));  // "Uefa Champions League"

// String checks
let age = "9089";
console.log(/^\d+$/.test(age));  // true (regex check)

// Type conversion
let ageNum = 45;
console.log(String(ageNum));  // "45"

// String slicing (substring)
let greeting = "Hello, good morning";
console.log(greeting);  // Full string
console.log(greeting.split("").reverse().join(""));  // Reversed: "gninrom doog ,olleH"

// String trimming
let username = "  chris.idakwo@email.com  ";
console.log(username.trim());        // "chris.idakwo@email.com"
console.log(username.trimStart());   // "chris.idakwo@email.com  "
console.log(username.trimEnd());     // "  chris.idakwo@email.com"

// String concatenation
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName;

// String formatting (template literals)
let score = 80;
let sentence = `${firstName} ${lastName} scored ${score} out of 100`;
```

**Key Differences:**
- Python uses `len()`, JavaScript uses `.length` property
- Python methods: `.lower()`, `.upper()`, `.strip()`
- JavaScript methods: `.toLowerCase()`, `.toUpperCase()`, `.trim()`
- Python f-strings use `f"..."`, JavaScript template literals use `` `${...}` ``
- Python string slicing uses `[start:end:step]`, JavaScript uses `.substring()`, `.slice()`, or `.substr()`

---

### Math Operations

**Python Concept:**
Python supports all standard arithmetic operations following BODMAS (order of operations).

**Python Example:**
```python
# Addition
print(1 + 5)        # 6
print(-5 + 7)       # 2

# Subtraction
print(4 - 5)        # -1
print(84 - 29)      # 55

# Multiplication
print(2 * 2)        # 4
print(3.14 * 2)     # 6.28

# Division (always returns float)
print(4 / 2)        # 2.0
print(98.45 / 3.75) # 26.253333...

# Exponentiation
print(2 ** 3)       # 8
print(4 ** 3)       # 64

# Modulus (remainder)
print(3 % 2)        # 1

# Order of operations
print(4 + 6 - 2 / 4)      # 9.5
print(4 + (6 - 2) / 4)    # 5.0
```

**JavaScript Equivalent:**
```javascript
// Addition
console.log(1 + 5);        // 6
console.log(-5 + 7);       // 2

// Subtraction
console.log(4 - 5);        // -1
console.log(84 - 29);      // 55

// Multiplication
console.log(2 * 2);        // 4
console.log(3.14 * 2);     // 6.28

// Division (returns number, can be float or integer)
console.log(4 / 2);        // 2
console.log(98.45 / 3.75); // 26.253333...

// Exponentiation
console.log(2 ** 3);       // 8 (ES2016+)
console.log(Math.pow(4, 3)); // 64 (older method)

// Modulus (remainder)
console.log(3 % 2);        // 1

// Order of operations
console.log(4 + 6 - 2 / 4);      // 9.5
console.log(4 + (6 - 2) / 4);    // 5
```

**Key Differences:**
- Python division `/` always returns float, JavaScript returns number (can be integer or float)
- Python uses `**` for exponentiation, JavaScript uses `**` (ES2016+) or `Math.pow()`
- Both follow the same order of operations (BODMAS/PEMDAS)

---

### User Input

**Python Concept:**
The `input()` function reads user input from the console. It always returns a string.

**Python Example:**
```python
first_name = input("What is your first name? ")
last_name = input("What is your last name? ")
score = input("What was your score? ")

# Input is always a string, convert if needed
score_num = float(score)
percentage = (score_num / 100) * 10

# Method chaining
email_address = input("Enter your email address: ").strip().replace("email", "outlook")
```

**JavaScript Equivalent:**
```javascript
// In Node.js environment
const readline = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout
});

readline.question("What is your first name? ", (firstName) => {
    readline.question("What is your last name? ", (lastName) => {
        readline.question("What was your score? ", (score) => {
            // Input is always a string, convert if needed
            let scoreNum = parseFloat(score);
            let percentage = (scoreNum / 100) * 10;
            
            readline.close();
        });
    });
});

// In browser environment
let firstName = prompt("What is your first name? ");
let lastName = prompt("What is your last name? ");
let score = prompt("What was your score? ");

// Method chaining
let emailAddress = prompt("Enter your email address: ").trim().replace("email", "outlook");
```

**Key Differences:**
- Python `input()` is synchronous and simple
- JavaScript in Node.js requires `readline` module (async)
- JavaScript in browser uses `prompt()` (synchronous but blocks UI)
- Python uses `float()`, JavaScript uses `parseFloat()`
- Python uses `.strip()`, JavaScript uses `.trim()`

---

## Week 4 - Control Flows

### Comparison Operators

**Python Concept:**
Comparison operators compare two values and return a boolean (`True` or `False`).

**Python Example:**
```python
# Equal to
print(5 == 5)   # True

# Not equal to
print(5 != 5)   # False

# Greater than
print(7 > 10)   # False

# Less than
print(7 < 10)   # True

# Greater than or equal to
print(7 >= 10)  # False

# Less than or equal to
print(7 <= 10)  # True
```

**JavaScript Equivalent:**
```javascript
// Equal to
console.log(5 == 5);   // true (loose equality)
console.log(5 === 5);  // true (strict equality - recommended)

// Not equal to
console.log(5 != 5);   // false (loose)
console.log(5 !== 5);  // false (strict - recommended)

// Greater than
console.log(7 > 10);   // false

// Less than
console.log(7 < 10);   // true

// Greater than or equal to
console.log(7 >= 10);  // false

// Less than or equal to
console.log(7 <= 10);  // true
```

**Key Differences:**
- Python uses `==` and `!=` (only one type)
- JavaScript has `==`/`!=` (loose) and `===`/`!==` (strict - checks type too)
- Python uses `True`/`False`, JavaScript uses `true`/`false` (lowercase)
- JavaScript strict equality (`===`) is recommended to avoid type coercion issues

---

### Logical Operators

**Python Concept:**
Logical operators combine or modify boolean expressions.

**Python Example:**
```python
age = 25
has_id = True
is_student = False

# AND operator - all conditions must be true
if age >= 18 and has_id:
    print("Give access!")

# OR operator - at least one condition must be true
if age >= 18 or has_id:
    print("Give access!")

# NOT operator - negates the condition
logged_in = False
if not logged_in:
    print("You're a guest")

# Complex conditions
if age >= 60 or is_student:
    print("Yay, discount applied!")
```

**JavaScript Equivalent:**
```javascript
let age = 25;
let hasId = true;
let isStudent = false;

// AND operator - all conditions must be true
if (age >= 18 && hasId) {
    console.log("Give access!");
}

// OR operator - at least one condition must be true
if (age >= 18 || hasId) {
    console.log("Give access!");
}

// NOT operator - negates the condition
let loggedIn = false;
if (!loggedIn) {
    console.log("You're a guest");
}

// Complex conditions
if (age >= 60 || isStudent) {
    console.log("Yay, discount applied!");
}
```

**Key Differences:**
- Python uses `and`, `or`, `not` (keywords)
- JavaScript uses `&&`, `||`, `!` (symbols)
- Both follow short-circuit evaluation (stop evaluating once result is determined)

---

### If/Else Statements

**Python Concept:**
Conditional statements allow code to execute based on conditions.

**Python Example:**
```python
light = input("What color is the traffic light? ").lower()

if light == "green" or light == "blinking":
    print("Go")
elif light == "yellow":
    print("Slow down")
else:
    print("Stop")

# Nested if statements
temperature = 15
humidity = 15

if temperature > 30 or humidity < 20:
    print("Warning: Unusual weather condition detected!")
else:
    print("Weather conditions are normal")
```

**JavaScript Equivalent:**
```javascript
let light = prompt("What color is the traffic light? ").toLowerCase();

if (light === "green" || light === "blinking") {
    console.log("Go");
} else if (light === "yellow") {
    console.log("Slow down");
} else {
    console.log("Stop");
}

// Nested if statements
let temperature = 15;
let humidity = 15;

if (temperature > 30 || humidity < 20) {
    console.log("Warning: Unusual weather condition detected!");
} else {
    console.log("Weather conditions are normal");
}
```

**Key Differences:**
- Python uses `elif`, JavaScript uses `else if`
- Python uses colons `:` and indentation, JavaScript uses curly braces `{}`
- Python doesn't require parentheses around conditions (but can use them), JavaScript requires parentheses

---

### Input Validation

**Python Concept:**
Validating user input ensures data meets expected criteria before processing.

**Python Example:**
```python
light = input("What color is the traffic light? ").lower()

# Validate input
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

# Score validation
student_score = float(input("Enter score: "))
while student_score < 0 or student_score > 100:
    print("Invalid score! Please enter a score between 0 and 100")
    student_score = float(input("Enter score: "))
```

**JavaScript Equivalent:**
```javascript
let light = prompt("What color is the traffic light? ").toLowerCase();

// Validate input
let allowedColors = ["red", "yellow", "green", "blinking"];
if (allowedColors.includes(light)) {
    if (light === "green" || light === "blinking") {
        console.log("Go");
    } else if (light === "yellow") {
        console.log("Slow down");
    } else {
        console.log("Stop");
    }
} else {
    console.log("Valid colors are red, green, yellow, and blinking ONLY!");
}

// Score validation
let studentScore = parseFloat(prompt("Enter score: "));
while (studentScore < 0 || studentScore > 100) {
    console.log("Invalid score! Please enter a score between 0 and 100");
    studentScore = parseFloat(prompt("Enter score: "));
}
```

**Key Differences:**
- Python uses `in` operator for membership, JavaScript uses `.includes()` method
- Both use `while` loops for validation, syntax differs slightly

---

## Week 4 - Lists

### List Introduction

**Python Concept:**
Lists are ordered, mutable collections that can hold multiple values of any type.

**Python Example:**
```python
# List of numbers
scores = [56, 90, 34, 75, 45, 89, 65, 45]

# List of strings
shopping = ["rice", "milk", "bread", "eggs", "butter"]

# Mixed data types (not recommended but possible)
mixed = ["John", 25, False, 3.14, ["Chris"]]

# Empty list
empty_list = []

# Lists are mutable
scores.append(100)  # Add item
scores.remove(45)   # Remove item
```

**JavaScript Equivalent:**
```javascript
// Array of numbers
let scores = [56, 90, 34, 75, 45, 89, 65, 45];

// Array of strings
let shopping = ["rice", "milk", "bread", "eggs", "butter"];

// Mixed data types (common in JavaScript)
let mixed = ["John", 25, false, 3.14, ["Chris"]];

// Empty array
let emptyArray = [];

// Arrays are mutable
scores.push(100);  // Add item
scores.splice(scores.indexOf(45), 1);  // Remove first occurrence of 45
```

**Key Differences:**
- Python calls them "lists", JavaScript calls them "arrays"
- Python uses `.append()`, JavaScript uses `.push()`
- Python uses `.remove()`, JavaScript uses `.splice()` or `.filter()`
- Both are zero-indexed and mutable

---

### Accessing List Items

**Python Concept:**
List items are accessed using index positions. Python supports negative indexing.

**Python Example:**
```python
names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah"]

# Positive indexing (starts at 0)
print(names[0])   # "Mike" (first item)
print(names[1])   # "Jane" (second item)
print(names[2])   # "Blessing" (third item)

# Negative indexing (starts at -1 from the end)
print(names[-1])  # "Sarah" (last item)
print(names[-2])  # "Joe" (second to last)

# Length of list
print(len(names))  # 6
```

**JavaScript Equivalent:**
```javascript
let names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah"];

// Positive indexing (starts at 0)
console.log(names[0]);   // "Mike" (first item)
console.log(names[1]);   // "Jane" (second item)
console.log(names[2]);   // "Blessing" (third item)

// Negative indexing (not directly supported, use length)
console.log(names[names.length - 1]);  // "Sarah" (last item)
console.log(names[names.length - 2]);  // "Joe" (second to last)

// Length of array
console.log(names.length);  // 6
```

**Key Differences:**
- Python supports negative indexing directly (`-1` for last item)
- JavaScript requires `array.length - 1` to access last item
- Python uses `len()`, JavaScript uses `.length` property
- Both are zero-indexed

---

### List Slicing

**Python Concept:**
Slicing extracts a portion of a list using `[start:end:step]` syntax.

**Python Example:**
```python
names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah", "Chris", "Daniel"]

# Get items from index 2 to 6 (end index is exclusive)
print(names[2:6])  # ["Blessing", "Peter", "Joe", "Sarah"]

# Get all items
print(names[:])  # Full list

# Get items from start to index 4
print(names[:4])  # ["Mike", "Jane", "Blessing", "Peter"]

# Get items from index 2 to end
print(names[2:])  # ["Blessing", "Peter", "Joe", "Sarah", "Chris", "Daniel"]

# Step slicing
print(names[::2])  # Every 2nd item: ["Mike", "Blessing", "Joe", "Chris"]
```

**JavaScript Equivalent:**
```javascript
let names = ["Mike", "Jane", "Blessing", "Peter", "Joe", "Sarah", "Chris", "Daniel"];

// Get items from index 2 to 6 (end index is exclusive)
console.log(names.slice(2, 6));  // ["Blessing", "Peter", "Joe", "Sarah"]

// Get all items (shallow copy)
console.log(names.slice());  // Full list (copy)

// Get items from start to index 4
console.log(names.slice(0, 4));  // ["Mike", "Jane", "Blessing", "Peter"]

// Get items from index 2 to end
console.log(names.slice(2));  // ["Blessing", "Peter", "Joe", "Sarah", "Chris", "Daniel"]

// Step slicing (requires manual implementation or filter)
console.log(names.filter((_, index) => index % 2 === 0));  // Every 2nd item
```

**Key Differences:**
- Python uses `[start:end:step]`, JavaScript uses `.slice(start, end)`
- Python supports step parameter directly, JavaScript requires `.filter()` or manual loop
- Python slicing is more concise and powerful

---

## Week 4 - Loops

### For Loops

**Python Concept:**
For loops iterate over sequences (strings, lists, ranges, etc.).

**Python Example:**
```python
# Iterate over string
name = "Chris Idakwo"
for char in name:
    print(char)

# Iterate over range
for num in range(1, 6):
    print(num)  # Prints 1, 2, 3, 4, 5

# Iterate over list
names = ["Mike", "Jane", "Blessing"]
for name in names:
    print(name)

# Iterate with index
for index, name in enumerate(names):
    print(f"{index}: {name}")
```

**JavaScript Equivalent:**
```javascript
// Iterate over string
let name = "Chris Idakwo";
for (let char of name) {
    console.log(char);
}

// Iterate over range (requires manual implementation)
for (let num = 1; num < 6; num++) {
    console.log(num);  // Prints 1, 2, 3, 4, 5
}

// Iterate over array
let names = ["Mike", "Jane", "Blessing"];
for (let name of names) {
    console.log(name);
}

// Iterate with index
for (let index = 0; index < names.length; index++) {
    console.log(`${index}: ${names[index]}`);
}

// Or using forEach
names.forEach((name, index) => {
    console.log(`${index}: ${name}`);
});
```

**Key Differences:**
- Python `range()` is built-in, JavaScript uses traditional `for` loop or `Array.from()`
- Python `enumerate()` provides index-value pairs, JavaScript uses traditional loop or `.forEach()`
- Python `for...in` iterates over items, JavaScript `for...of` iterates over values
- JavaScript also has `.forEach()`, `.map()`, `.filter()` array methods

---

### While Loops

**Python Concept:**
While loops execute code repeatedly as long as a condition is true.

**Python Example:**
```python
# Count from 1 to 20
count = 1
while count <= 20:
    print(count)
    count = count + 1  # or count += 1

print("I'm outside the while loop")

# Flag-controlled loop
found = False
attempts = 0
while not found and attempts < 5:
    guess = input("Guess the number: ")
    if guess == "42":
        found = True
        print("Correct!")
    attempts += 1
```

**JavaScript Equivalent:**
```javascript
// Count from 1 to 20
let count = 1;
while (count <= 20) {
    console.log(count);
    count = count + 1;  // or count++
}

console.log("I'm outside the while loop");

// Flag-controlled loop
let found = false;
let attempts = 0;
while (!found && attempts < 5) {
    let guess = prompt("Guess the number: ");
    if (guess === "42") {
        found = true;
        console.log("Correct!");
    }
    attempts++;
}
```

**Key Differences:**
- Syntax is very similar between both languages
- Python uses `not`, JavaScript uses `!`
- Python uses `+=`, JavaScript uses `++` or `+=`
- Both support `do...while` (JavaScript) / `while True` with break (Python)

---

### Break Statement

**Python Concept:**
The `break` statement exits the loop immediately when encountered.

**Python Example:**
```python
# Exit loop when condition is met
for num in range(1, 1001):
    guess = int(input("Guess the number: "))
    if guess == 42:
        print("Correct! You've found the number 42")
        break  # Exit the loop
    print("Try again!")

# Break with condition
for num in range(1, 1001):
    if num > 20:
        break  # Exit when num exceeds 20
    if num % 2 == 0:
        print(num)
```

**JavaScript Equivalent:**
```javascript
// Exit loop when condition is met
for (let num = 1; num <= 1000; num++) {
    let guess = parseInt(prompt("Guess the number: "));
    if (guess === 42) {
        console.log("Correct! You've found the number 42");
        break;  // Exit the loop
    }
    console.log("Try again!");
}

// Break with condition
for (let num = 1; num <= 1000; num++) {
    if (num > 20) {
        break;  // Exit when num exceeds 20
    }
    if (num % 2 === 0) {
        console.log(num);
    }
}
```

**Key Differences:**
- Syntax is identical: `break` in both languages
- Works the same way in both languages

---

### Continue Statement

**Python Concept:**
The `continue` statement skips the rest of the current iteration and moves to the next one.

**Python Example:**
```python
# Skip even numbers, print only odds
for num in range(1, 11):
    if num % 2 == 0:
        continue  # Skip this iteration
    print(num)  # Only prints odd numbers: 1, 3, 5, 7, 9
```

**JavaScript Equivalent:**
```javascript
// Skip even numbers, print only odds
for (let num = 1; num <= 10; num++) {
    if (num % 2 === 0) {
        continue;  // Skip this iteration
    }
    console.log(num);  // Only prints odd numbers: 1, 3, 5, 7, 9
}
```

**Key Differences:**
- Syntax is identical: `continue` in both languages
- Works the same way in both languages

---

## Week 5 - Dictionaries

### Dictionary Introduction

**Python Concept:**
Dictionaries store data in key-value pairs. Keys must be unique and immutable (usually strings).

**Python Example:**
```python
# Dictionary literal
student_a = {
    "first_name": "Chris",
    "last_name": "Idakwo",
    "age": 20,
    "height": 1.65,
    "gender": "Male",
    "registered": True,
    "skills": []
}

# Dictionary constructor
student_b = dict(
    first_name="Chris",
    last_name="Idakwo",
    age=20,
    height=1.65,
    gender="Male"
)

# Empty dictionary
empty_dict = {}

# Dictionaries are mutable
student_a["email"] = "chris@example.com"  # Add new key-value
student_a["age"] = 21  # Update existing value
```

**JavaScript Equivalent:**
```javascript
// Object literal
let studentA = {
    firstName: "Chris",
    lastName: "Idakwo",
    age: 20,
    height: 1.65,
    gender: "Male",
    registered: true,
    skills: []
};

// Object constructor (less common)
let studentB = new Object();
studentB.firstName = "Chris";
studentB.lastName = "Idakwo";
studentB.age = 20;

// Empty object
let emptyObj = {};

// Objects are mutable
studentA.email = "chris@example.com";  // Add new property
studentA.age = 21;  // Update existing property
```

**Key Differences:**
- Python uses "dictionaries", JavaScript uses "objects"
- Python keys are usually strings in quotes, JavaScript keys can be unquoted (if valid identifiers)
- Python uses `dict()`, JavaScript uses `{}` or `new Object()`
- Python uses `True`/`False`, JavaScript uses `true`/`false`
- Both are mutable and support nested structures

---

### Accessing Dictionary Values

**Python Concept:**
Access dictionary values using square brackets with the key name.

**Python Example:**
```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "engineLitre": 5.0,
    "transmission": "manual"
}

# Access single value
trans = car["transmission"]
print(trans)  # "manual"

# Nested dictionary access
person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50,
    "pets": {"dog": "Frieda", "cat": "Sox"},
    "kids": ["Joe", "Martha", "Sarah"]
}

# Access nested dictionary
dog_name = person["pets"]["dog"]
print(dog_name)  # "Frieda"

# Access list within dictionary
second_child = person["kids"][1]
print(second_child)  # "Martha"
```

**JavaScript Equivalent:**
```javascript
let car = {
    brand: "Ford",
    model: "Mustang",
    engineLitre: 5.0,
    transmission: "manual"
};

// Access single value (bracket notation)
let trans = car["transmission"];
console.log(trans);  // "manual"

// Or dot notation
let trans2 = car.transmission;
console.log(trans2);  // "manual"

// Nested object access
let person = {
    firstName: "John",
    lastName: "Doe",
    age: 50,
    pets: {dog: "Frieda", cat: "Sox"},
    kids: ["Joe", "Martha", "Sarah"]
};

// Access nested object
let dogName = person.pets.dog;  // or person["pets"]["dog"]
console.log(dogName);  // "Frieda"

// Access array within object
let secondChild = person.kids[1];  // or person["kids"][1]
console.log(secondChild);  // "Martha"
```

**Key Differences:**
- Python only uses bracket notation: `dict["key"]`
- JavaScript supports both: `obj.key` (dot notation) and `obj["key"]` (bracket notation)
- Both support nested access with chaining

---

### Dictionary Methods

**Python Concept:**
Dictionaries have built-in methods for common operations.

**Python Example:**
```python
from pprint import pprint

person = {
    "first_name": "John",
    "last_name": "Doe",
    "age": 50,
    "pets": {"dog": "Frieda", "cat": "Sox"},
    "kids": ["Joe", "Martha", "Sarah"]
}

# get() - Returns value or None if key doesn't exist
first_name = person.get("first_name")  # "John"
middle_name = person.get("middle_name")  # None (no error)

# keys() - Returns all keys
print(person.keys())  # dict_keys(['first_name', 'last_name', ...])

# values() - Returns all values
print(person.values())  # dict_values(['John', 'Doe', 50, ...])

# items() - Returns key-value pairs as tuples
print(person.items())  # dict_items([('first_name', 'John'), ...])

# pop() - Removes and returns value
last_name = person.pop("last_name")  # Removes "last_name" key
print(last_name)  # "Doe"

# copy() - Creates shallow copy
person_copy = person.copy()

# clear() - Removes all items
person_copy.clear()  # {}
```

**JavaScript Equivalent:**
```javascript
let person = {
    firstName: "John",
    lastName: "Doe",
    age: 50,
    pets: {dog: "Frieda", cat: "Sox"},
    kids: ["Joe", "Martha", "Sarah"]
};

// Access property (similar to get())
let firstName = person.firstName;  // "John"
let middleName = person.middleName;  // undefined (no error)

// Object.keys() - Returns all keys as array
console.log(Object.keys(person));  // ["firstName", "lastName", ...]

// Object.values() - Returns all values as array
console.log(Object.values(person));  // ["John", "Doe", 50, ...]

// Object.entries() - Returns key-value pairs as arrays
console.log(Object.entries(person));  // [["firstName", "John"], ...]

// delete operator - Removes property
let lastName = person.lastName;
delete person.lastName;  // Removes "lastName" property
console.log(lastName);  // "Doe"

// Object.assign() or spread - Creates shallow copy
let personCopy = {...person};  // or Object.assign({}, person)

// Clear object (manual)
Object.keys(personCopy).forEach(key => delete personCopy[key]);
// Or reassign
personCopy = {};
```

**Key Differences:**
- Python methods are called on the dictionary: `dict.get()`, `dict.keys()`
- JavaScript uses `Object` static methods: `Object.keys()`, `Object.values()`
- Python `.get()` returns `None` for missing keys, JavaScript returns `undefined`
- Python `.pop()` removes and returns, JavaScript uses `delete` operator
- Python `.copy()` creates copy, JavaScript uses spread `{...obj}` or `Object.assign()`
- Python `.clear()` empties dict, JavaScript requires manual deletion or reassignment

---

### Dictionary Operations

**Python Concept:**
Dictionaries support various operations for manipulation and iteration.

**Python Example:**
```python
# Adding/Updating items
student = {"name": "John", "age": 20}
student["email"] = "john@example.com"  # Add
student["age"] = 21  # Update

# Checking if key exists
if "name" in student:
    print("Name exists")

# Iterating over dictionary
for key in student:
    print(f"{key}: {student[key]}")

# Iterating over items
for key, value in student.items():
    print(f"{key}: {value}")

# Dictionary comprehension (advanced)
squared = {x: x**2 for x in range(5)}  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

**JavaScript Equivalent:**
```javascript
// Adding/Updating properties
let student = {name: "John", age: 20};
student.email = "john@example.com";  // Add
student.age = 21;  // Update

// Checking if property exists
if ("name" in student) {
    console.log("Name exists");
}

// Or using hasOwnProperty
if (student.hasOwnProperty("name")) {
    console.log("Name exists");
}

// Iterating over object
for (let key in student) {
    console.log(`${key}: ${student[key]}`);
}

// Iterating over entries
for (let [key, value] of Object.entries(student)) {
    console.log(`${key}: ${value}`);
}

// Object creation with computed properties (ES6)
let squared = {};
for (let x = 0; x < 5; x++) {
    squared[x] = x ** 2;
}
// Or using Object.fromEntries
let squared2 = Object.fromEntries(
    Array.from({length: 5}, (_, x) => [x, x ** 2])
);
```

**Key Differences:**
- Python uses `in` operator for membership, JavaScript uses `in` or `.hasOwnProperty()`
- Python `.items()` returns tuples, JavaScript `Object.entries()` returns arrays
- Python has dictionary comprehensions, JavaScript requires manual construction or `Object.fromEntries()`
- Both support iteration and dynamic property addition/updates

---

## Week 5 - Working with Files

### File Introduction

**Python Concept:**
Python uses the built-in `open()` function to work with files. Files must be opened with a mode (read, write, append) and closed when done.

**Python Example:**
```python
# Open file for reading (default mode)
file = open("example.txt")
content = file.read()
file.close()

# Using with statement (recommended - auto-closes)
with open("example.txt") as f:
    content = f.read()
```

**JavaScript Equivalent (Node.js):**
```javascript
const fs = require('fs');
let content = fs.readFileSync('example.txt', 'utf8');
// Or async: fs.promises.readFile('example.txt', 'utf8')
```

**Key Differences:**
- Python uses `open()` with mode strings (`'r'`, `'w'`, `'a'`), Node.js uses `fs.readFileSync`/`fs.writeFileSync` or async variants
- Python's `with` statement ensures files are closed; JavaScript relies on sync/async APIs
- Python has `csv` module for CSV; Node.js often uses packages like `csv-parse`

---

### Reading from Files

**Python Concept:**
Use `.read()` to get the entire file content as a string, or `.readline()`/`.readlines()` for line-by-line reading.

**Python Example:**
```python
with open("greeting.txt") as f:
    content = f.read()  # Entire file as string
    # Or: line = f.readline()  # One line
    # Or: lines = f.readlines()  # List of lines
```

---

### Reading File Lines

**Python Concept:**
Iterate over the file object directly to read line by line without loading the whole file into memory.

**Python Example:**
```python
with open("log.txt") as f:
    for line in f:
        print(line.strip())
```

---

### Writing to Files

**Python Concept:**
Open with mode `'w'` to write (overwrites existing content). Use `.write()` or `.writelines()`.

**Python Example:**
```python
with open("output.txt", "w") as f:
    f.write("Hello, World!\n")
    f.writelines(["Line 1\n", "Line 2\n"])
```

**JavaScript Equivalent (Node.js):**
```javascript
fs.writeFileSync('output.txt', 'Hello, World!\n');
```

---

### Appending to Files

**Python Concept:**
Open with mode `'a'` to append without overwriting existing content.

**Python Example:**
```python
with open("log.txt", "a") as f:
    f.write("New log entry\n")
```

---

### Processing CSV Data

**Python Concept:**
The `csv` module provides `reader` and `writer` for reading and writing CSV files.

**Python Example:**
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

**Python Concept:**
Functions are defined with `def` followed by the function name and parameters in parentheses.

**Python Example:**
```python
def greet(name):
    print(f"Hello, {name}!")

greet("Chris")
```

**JavaScript Equivalent:**
```javascript
function greet(name) {
    console.log(`Hello, ${name}!`);
}
greet("Chris");
```

**Key Differences:**
- Python uses `def`, JavaScript uses `function` or arrow functions `() =>`
- Python has no curly braces; indentation defines the body
- Both support default parameters and multiple return values (Python via tuples, JS via destructuring)

---

### Return Values

**Python Concept:**
Use `return` to send a value back from a function. Without `return`, the function returns `None`.

**Python Example:**
```python
def add(a, b):
    return a + b

result = add(3, 5)  # 8
```

---

### Default Parameters

**Python Concept:**
Parameters can have default values; callers can omit those arguments.

**Python Example:**
```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

print(greet("Chris"))           # Hello, Chris!
print(greet("Chris", "Hi"))     # Hi, Chris!
```

**JavaScript Equivalent:**
```javascript
function greet(name, greeting = "Hello") {
    return `${greeting}, ${name}!`;
}
```

---

### Positional and Keyword Arguments

**Python Concept:**
Arguments can be passed by position or by name (keyword). Keyword arguments often follow positional ones.

**Python Example:**
```python
def describe(name, age, city="Lagos"):
    return f"{name}, {age}, from {city}"

describe("John", 30)
describe("John", 30, city="Abuja")
describe(age=25, name="Jane", city="Kano")
```

---

### Return Multiple Values

**Python Concept:**
Functions can return multiple values as a tuple; callers can unpack them.

**Python Example:**
```python
def min_max(numbers):
    return min(numbers), max(numbers)

low, high = min_max([3, 1, 4, 1, 5])
```

**JavaScript Equivalent:**
```javascript
function minMax(numbers) {
    return [Math.min(...numbers), Math.max(...numbers)];
}
const [low, high] = minMax([3, 1, 4, 1, 5]);
```

---

### Variable Scope

**Python Concept:**
Variables defined inside a function are local. Global variables can be read inside a function; use `global` to modify them.

**Python Example:**
```python
count = 0  # Global

def increment():
    global count
    count += 1

increment()
print(count)  # 1
```

---

## Week 7 - Advanced Working with Files

### Reading from CSV Files

**Python Concept:**
Use `csv.reader()` for list rows or `csv.DictReader()` for rows as dictionaries with headers as keys.

**Python Example:**
```python
import csv
with open("students_grades.csv", newline='') as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(row["name"], row["grade"])
```

---

### Writing to CSV Files

**Python Concept:**
Use `csv.writer()` or `csv.DictWriter()` to write CSV data.

**Python Example:**
```python
import csv
with open("output.csv", "w", newline='') as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Score"])
    writer.writerows([["Alice", 95], ["Bob", 87]])
```

---

### CSV Quotes

**Python Concept:**
The `csv` module handles quoting with `quoting` and `quotechar`. Use `csv.QUOTE_MINIMAL`, `QUOTE_ALL`, etc.

**Python Example:**
```python
import csv
with open("data.csv", "w", newline='') as f:
    writer = csv.writer(f, quoting=csv.QUOTE_MINIMAL)
    writer.writerow(["Name", "Description"])
```

---

### Working with OS Module

**Python Concept:**
The `os` module provides path and environment operations: `os.path.exists()`, `os.listdir()`, `os.getcwd()`, `os.path.join()`, etc.

**Python Example:**
```python
import os
print(os.getcwd())
print(os.listdir("."))
path = os.path.join("folder", "file.txt")
if os.path.exists(path):
    print("File exists")
```

**JavaScript Equivalent (Node.js):**
```javascript
const path = require('path');
const fs = require('fs');
console.log(process.cwd());
console.log(fs.readdirSync('.'));
const p = path.join('folder', 'file.txt');
if (fs.existsSync(p)) console.log('File exists');
```

---

### Directory Utilities

**Python Concept:**
Combine `os` and `os.path` to list directories, check file types, and build paths for file processing.

**Python Example:**
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

1. **Basics**: Variables, data types (numbers, strings), operations, and input handling
2. **Control Flow**: Conditional statements, comparison and logical operators
3. **Data Structures**: Lists (arrays) and Dictionaries (objects)
4. **Loops**: For loops, while loops, and loop control (break/continue)
5. **Working with Files**: Reading, writing, appending, and processing CSV data
6. **Functions**: Defining functions, return values, default parameters, scope
7. **Advanced Files**: CSV reader/writer, quoting, `os` module, directory utilities

### Key Python vs JavaScript Differences:

| Feature | Python | JavaScript |
|---------|--------|------------|
| Variable Declaration | No keyword needed | `let`, `const`, `var` |
| String Methods | `.lower()`, `.upper()` | `.toLowerCase()`, `.toUpperCase()` |
| String Formatting | f-strings `f"..."` | Template literals `` `${...}` `` |
| Division | Always returns float | Returns number (int or float) |
| Exponentiation | `**` | `**` or `Math.pow()` |
| Comparison | `==`, `!=` | `==`, `!=` (loose) or `===`, `!==` (strict) |
| Logical Operators | `and`, `or`, `not` | `&&`, `||`, `!` |
| Conditionals | `if`, `elif`, `else` | `if`, `else if`, `else` |
| Lists/Arrays | `.append()`, `.remove()` | `.push()`, `.splice()` |
| Negative Indexing | Direct support `[-1]` | `array[array.length - 1]` |
| Slicing | `[start:end:step]` | `.slice(start, end)` |
| For Loops | `for item in iterable` | `for (let item of array)` |
| Dictionaries/Objects | `dict["key"]` | `obj.key` or `obj["key"]` |
| Dictionary Methods | `.get()`, `.keys()`, `.items()` | `Object.keys()`, `Object.entries()` |

Both languages are powerful and have their strengths. Python is often preferred for data science and backend development, while JavaScript is essential for web development. Understanding both helps you become a more versatile programmer!
