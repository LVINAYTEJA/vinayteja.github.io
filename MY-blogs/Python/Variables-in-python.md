# Variables in Python
A **variable** in Python is a name that stores a value. It acts as a container that holds data, which can be changed during program execution.
## Variable Declaration in Python
Unlike some programming languages, Python does not require you to declare a variable type explicitly. You can simply assign a value to a variable.
### **Example:**
```python
# Assigning values to variables
name = "Arjun"
age = 22
pi = 3.14159

print(name)  # Output: Alice
print(age)   # Output: 25
print(pi)    # Output: 3.14159
```
## Variable Naming Rules
Python variable names must follow these rules:
1. Can contain letters, numbers, and underscores ( _ ).
2. Must start with a letter or an underscore ( _ ).
3. Cannot start with a number.
4. Cannot use Python keywords (if, else, while, etc.).
### Valid Examples
```python
first_name = "John"
_age = 30
PI = 3.14
```
### Invalid Examples
```python
1name = "John"
first-name = "John"
if = 10
```
## Reassigning Variables
You can change the value of a variable at any time.
```python
x = 10
print(x)  # Output: 10

x = "Python"
print(x)  # Output: Python
```
Python is dynamically typed, which means that you don’t need to declare the type explicitly.
## Multiple Assignments
Python allows assigning multiple variables in a single line.
```python
a, b, c = 5, 10, 15
print(a, b, c)  # Output: 5 10 15
```
You can also assign the same value to multiple variables.
```python
x = y = z = "Python"
print(x, y, z)  # Output: Python Python Python
```
## Constants in Python
Python does not have built-in constant types, but by convention, constants are written in UPPERCASE.
```python
PI = 3.14159
GRAVITY = 9.8
```
Although Python does not enforce constants, writing them in uppercase helps other programmers understand that they should not be modified.
#
👉 Previous:[My First Program](my-first-program.md) 👉 Next:[Types of Variables in Python](Types-of-variables.md)
