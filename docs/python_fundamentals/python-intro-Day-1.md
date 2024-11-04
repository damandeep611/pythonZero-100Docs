---
title: Python Intro and basic syntax
sidebar_position: 1
---

# Python Basic syntax

## Install Python and Setup IDE

To get started with Python, you'll need to:

1. Install Python on your system
2. Set up an Integrated Development Environment (IDE)
   - Recommended options: PyCharm or Visual Studio Code (VS Code)

## What are Variables in Python and How We Use Them?

Variables in Python are used to assign values to elements. Here's how we use them:

```python
name = "alice"  # normal syntax method to define a variable
age = 29  # syntax to define a number
salary = 1890.33  # to define a floating point number
is_trading = True  # to declare a boolean type 

print(name)
# this is how you write a variable and then print it using print function
```

## Constants in python 
Constants are values like variables, but the values in constants shouldn't be changed during program execution, well python doesn't have a different syntax to declare constants but it has a convention to declare constant value i.e naming constant as ALL_CAPS

```python 
PI = 3.14159
MAX_CONNECTIONS = 100
DATABASE_URL = "mongodb://localhost:27017"
```

One key difference to note is that while you can change a variable's value throughout your code, constants should remain unchanged after their initial assignment to maintain good programming practices.

### New Syntax for Type Hinting

```python
last_name: str = "jones" 
# this is also a new syntax way to define a variable when you have to explicitly define a variable with a type
```

### Printing Multiple Variables

```python
# syntax to use when we want to print multiple variables all at once with some string 
print(f"my name is {name}, and my age is {age}. i have salary of {salary}")
```

The `f` is for format string and it allows us to embed the variables inside the string. We can also format the price to 2 decimal places:

```python
price = 19.99
print(f"Hello {name}, you are {age} years old and the price is {price:.2f}")
```

We can also use the `round` function to round the price to 2 decimal places:

```python
print(f"Hello {name}, you are {age} years old and the price is {round(price, 2)} and is trading {is_trading}")
```

## Data Types in Python

### 1. Integers
Whole numbers, i.e., 5, 10, -3, 0

```python
x = 3
y = 10
j = -3
print(f"the three integers {x, y, j}")
```

### 2. Floating Point Numbers
Decimal numbers

```python
a = 3.1459
b = -0.5
c = 2.0

# Let's do some basic arithmetic operations
print(f"sum: {a + b}, product: {a * y}")

# complex is another data type 
z = 2 + 3j
```

### 3. Strings

```python
thisOne = "hello world"
name = "python"
full_string = thisOne + " " + name
print(full_string)

# some string methods - 
text = "Hello, World!"

# Common string methods
print(text.lower())       # hello, world!
print(text.upper())       # HELLO, WORLD!
print(text.split(","))    # ["Hello", " World!"]
print(text.strip())       # Removes whitespace
print(text.replace("Hello", "Hi"))  # Hi, World!

```

### 4. Booleans
To declare a value true or false

```python
tryThisOne = True

checkGreater = b > j
print(checkGreater)
```

### 5. Lists 
Ordered and mutable collections

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
numbers.append(12)
print(numbers)
# .append is one of many built-in functions that we use to operate on lists 

# Common list methods
numbers.append(6)      # Add to end
numbers.insert(0, 0)   # Insert at index
numbers.remove(3)      # Remove first occurrence
numbers.pop()          # Remove and return last item
numbers.sort()         # Sort in place
numbers.reverse()      # Reverse in place

# List comprehension
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]
```

### 6. Dictionaries
Combination of key-value pairs

```python
person = {
  "hero": "flash",
  "power": "superspeed",
  "universe": "DC",
  "age": 28
}

print(person)

# We can also perform operations on dictionaries
# To assign a new value 
person["multiverse"] = True
person["realName"] = "Barry Allen"
print(person)
```

## Lists and Tuples

### Lists (Mutable)

```python
performers = ["test", "hero", "slicer", "cutter"] 
performers[0] = "villan"
performers.append("neutral")
print(performers)

# Why lists are used:
# When we need to frequently add, remove or modify the elements in the lists
# e.g., a todo list application

todo_list = ["hiking App", "Trading App", "python trade"]
todo_list.append("portfolio website")
todo_list.remove("python trade")

print(todo_list)
```

### Tuples (Immutable)

```python
coordinates = (89.81, 45.89)
# coordinates[0] = 99  # this will throw errors 
print(coordinates)

# Trying to modify a tuple
try:
  coordinates[1] = 120
except TypeError as e:
  print(f"Error while modifying tuple is : {e}")

# Tuples can also be used as dictionary keys, because they're immutable 
locations = {
  (40.7128, 74.0060): "New York City",
  (34.0522, 118.2437): "Los Angeles"
}
```

Use tuples when you don't want the data to be changed accidentally, such as for user information or sensitive data stored in your application.

## Mnemonic: "FINS"

Remember the basic data types with "FINS":
- **F**loat
- **I**nteger
- **N**one
- **S**tring


## Exception handling in python 

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
except Exception as e:
    print(f"An error occurred: {e}")
finally:
    print("This always executes")

```

## some build in functions 

```python 

# len() - get length
print(len([1, 2, 3]))  # 3

# type() - get type
print(type(42))  # <class 'int'>

# input() - get user input
name = input("Enter your name: ")

# range() - generate sequence
for i in range(3):  # 0, 1, 2
    print(i)
```


some of the key points to remember in python - 

### Exercise: Calculate compound interest using variables and operations

so for day one we will make a compound interest calculator 