---
title: Python Introduction - Day 1
sidebar_position: 1
---

# Python Introduction - Day 1

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
```

### 3. Strings

```python
thisOne = "hello world"
name = "python"
full_string = thisOne + " " + name
print(full_string)
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

### Exercise: Calculate compound interest using variables and operations

Try creating a Python script that calculates compound interest using the concepts we've learned today!