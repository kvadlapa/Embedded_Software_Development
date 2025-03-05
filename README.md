# Embedded_Software_Development

## 1 Python
Here's a **Python Cheatsheet** covering essential syntax, data structures, and commonly used functions.

---

## **1.1 Basics**
```python
# Print
print("Hello, World!")

# Variables
x = 10        # Integer
y = 3.14      # Float
name = "Kiran" # String
is_valid = True # Boolean

# Multiple assignment
a, b, c = 1, 2, 3

# Comments
# Single-line comment
""" Multi-line
    comment """
```

---

## **1.2 Data Types & Type Conversion**
```python
# Checking Type
print(type(x))  # <class 'int'>

# Type Conversion
num = int("10")  # String to Integer
flt = float("3.14")  # String to Float
txt = str(100)  # Integer to String
```

---

## **1.3 Operators**
```python
# Arithmetic Operators
a + b  # Addition
a - b  # Subtraction
a * b  # Multiplication
a / b  # Division
a // b # Floor division
a ** b # Exponentiation
a % b  # Modulus

# Comparison Operators
a == b # Equal
a != b # Not equal
a > b  # Greater than
a < b  # Less than

# Logical Operators
and, or, not

# Membership Operators
'in', 'not in'
```

---

## **1.4 Strings**
```python
s = "Hello, World!"
print(s.lower())  # hello, world!
print(s.upper())  # HELLO, WORLD!
print(s.strip())  # Removes whitespace
print(s.replace("Hello", "Hi"))  # Hi, World!
print(s.split(","))  # ['Hello', ' World!']
print(s[0:5])  # Hello
print(len(s))  # Length of string
```

---

## **1.5 Lists (Arrays)**
```python
my_list = [1, 2, 3, "apple", True]
print(my_list[0])  # 1
print(my_list[-1])  # True

# List Methods
my_list.append(4)  # Add to end
my_list.insert(1, "banana")  # Insert at index
my_list.remove("apple")  # Remove item
my_list.pop()  # Remove last item
print(len(my_list))  # Length of list
my_list.sort()  # Sort list (for numbers or strings)
```

---

## **1.6 Tuples (Immutable Lists)**
```python
my_tuple = (1, 2, 3, "apple")
print(my_tuple[1])  # 2
```

---

## **1.7 Sets (Unique & Unordered)**
```python
my_set = {1, 2, 3, 4}
my_set.add(5)  # Add element
my_set.remove(2)  # Remove element
print(3 in my_set)  # Check membership
```

---

## **1.8 Dictionaries (Key-Value Pairs)**
```python
person = {"name": "Kiran", "age": 24}
print(person["name"])  # Kiran

# Add / Update
person["city"] = "New York"

# Dictionary Methods
print(person.keys())  # Get all keys
print(person.values())  # Get all values
```

---

## **1.9 Conditional Statements**
```python
age = 20
if age >= 18:
    print("Adult")
elif age > 13:
    print("Teenager")
else:
    print("Child")
```

---

## **1.10 Loops**
```python
# For Loop
for i in range(5):
    print(i)

# While Loop
x = 0
while x < 5:
    print(x)
    x += 1

# Looping over lists
for item in ["apple", "banana", "cherry"]:
    print(item)
```

---

## **1.11 Functions**
```python
def greet(name):
    return "Hello, " + name

print(greet("Kiran"))
```

---

## **1.12 Lambda (Anonymous Function)**
```python
square = lambda x: x ** 2
print(square(5))  # 25
```

---

## **1.13 Exception Handling**
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
finally:
    print("This runs no matter what.")
```

---

## **1.14 File Handling**
```python
# Read a file
with open("file.txt", "r") as file:
    print(file.read())

# Write to a file
with open("file.txt", "w") as file:
    file.write("Hello, World!")
```

---

## **1.15 List Comprehensions**
```python
numbers = [x for x in range(10) if x % 2 == 0]
print(numbers)  # [0, 2, 4, 6, 8]
```

---

## **1.16 Classes & Objects**
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}"

p1 = Person("Kiran", 24)
print(p1.greet())  # Hello, my name is Kiran
```

---

## **1.17 Modules**
```python
# Importing a module
import math
print(math.sqrt(16))  # 4.0
```

---

## **1.18 Useful Built-in Functions**
```python
print(abs(-5))  # Absolute value
print(sum([1, 2, 3]))  # Sum of list
print(max(1, 5, 3))  # Max value
print(min(1, 5, 3))  # Min value
print(round(3.14159, 2))  # 3.14
```

---

## **1.19 JSON Handling**
```python
import json

data = '{"name": "Kiran", "age": 24}'
parsed = json.loads(data)  # Convert JSON to dictionary
print(parsed["name"])  # Kiran

# Convert dictionary to JSON
json_data = json.dumps(parsed)
print(json_data)  # '{"name": "Kiran", "age": 24}'
```

---

## **1.20 Multi-threading**
```python
import threading

def print_numbers():
    for i in range(5):
        print(i)

t1 = threading.Thread(target=print_numbers)
t1.start()
t1.join()  # Wait for the thread to finish