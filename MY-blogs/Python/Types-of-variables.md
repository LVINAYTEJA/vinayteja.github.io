# Types of Variables in Python
In Python, variables are classified based on **scope** and **nature of assignment**. Understanding these classifications helps in writing efficient and error-free code.
## **1. Based on Scope**
Scope determines where a variable can be accessed.
### **a) Local Variables**
- Local variables are defined inside a function.
- These variables are only accessible within that function.
#### **Example**
```python
def greet():
    message = "Hello, Python!"  # Local variable
    print(message)

greet()
# print(message)  # Error: message is not accessible outside the function
```
### **b) Global Variables**
- Declared outside any function.
- Can be accessed anywhere in the program.
#### **Example**
```python
global_message = "I am global"

def display():
    print(global_message)  # Accessible inside the function

display()
print(global_message)  # Accessible outside the function
```
### Modifying Global Variables
To modify a global variable inside a function, use the **global** keyword.
```python
count = 0
def update_count():
    global count
    count += 1
update_count()
print(count)  # Output: 1
```
## **2. Based on Nature of Assignment**
Python variables can store different types of data.
### **a) Instance Variables (Object-Level)**
- Defined inside a class but within instance methods.
- Unique to each instance of the class.
#### **Example**
```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Instance variable
        self.age = age    # Instance variable
p1 = Person("Mahesh", 25)
p2 = Person("Bob", 30)
print(p1.name, p1.age)  # Output: Mahesh 25
print(p2.name, p2.age)  # Output: Bob 30
```
### **b) Class Variables (Shared Across Instances)**
- Defined inside a class but outside instance methods.
- Shared among all objects of the class.
#### **Example**
```python
class Student:
    school_name = "ABC School"  # Class variable
    def __init__(self, name):
        self.name = name  # Instance variable
s1 = Student("John")
s2 = Student("Emma")
print(s1.name, s1.school_name)  # Output: John ABC School
print(s2.name, s2.school_name)  # Output: Emma ABC School
```
### **c) Static Variables**
- Similar to class variables but defined using @staticmethod.
- Do not depend on instances.
#### **Example**
```python
class MathUtils:
    @staticmethod
    def add(a, b):
        return a + b

print(MathUtils.add(5, 10))  # Output: 15
```
## Summary
| Type	            | Scope	             | Defined Inside	        | Access                            |
|:-----------------:|:------------------:|:----------------------:|:---------------------------------:|
| Local Variable	  | Limited	           | Function	              | Inside function only              |
| Global Variable  	| Entire program     |	Outside functions	    | Anywhere                          |
| Nonlocal Variable	| Enclosing function |	Nested function       |	Inside enclosing function         |
| Instance Variable	| Object-Level       | Inside class           | (self.variable)	Unique per object |
| Class Variable	  | Shared	           | Inside class	          | Shared by all objects             |
| Static Variable	  | Independent        |	@staticmethod method	| Shared by all objects             |
# Conclusion
- Local, Global, and Nonlocal Variables are based on scope.
- Instance, Class, and Static Variables are based on object-oriented programming.
#
👉 Previous: [Variables in Python](Variables-in-python.md) 👉 Next: [Data Types](Data-types.md)
