# 🐍 Python Basics for Data Science

This document contains essential Python syntax and concepts frequently used in data science and machine learning.

---

## 🧮 Variables & Data Types

```python
x = 10              # Integer
pi = 3.14           # Float
name = "Hatice"     # String
is_ready = True     # Boolean
```

---

## 📚 Data Structures

### ✅ List

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits[1])  # banana
```

### ✅ Dictionary

```python
person = {"name": "Hatice", "age": 24}
print(person["name"])         # Hatice
person["age"] = 25
```

### ✅ Tuple

```python
dimensions = (1920, 1080)
print(dimensions[0])  # 1920
```

### ✅ Set

```python
unique_numbers = {1, 2, 3, 3}
print(unique_numbers)  # {1, 2, 3}
```

---

## 🔁 Loops

### For loop

```python
for i in range(5):
    print(i)
```

### While loop

```python
count = 0
while count < 3:
    print(count)
    count += 1
```

---

## ✅ Conditional Statements

```python
x = 5
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")
```

---

## 🔧 Functions

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Hatice"))
```

---

## 🧠 List Comprehension

```python
squares = [x ** 2 for x in range(5)]
print(squares)  # [0, 1, 4, 9, 16]
```

---

## 🔍 Useful Built-in Functions

```python
len([1, 2, 3])          # length of list - 3 
sum([1, 2, 3])          # summation of list - 6
sorted([3, 1, 2])       # sorted list - [1, 2, 3]
type(3.14)              # type of variable - <class 'float'>
```

---

## 🧪 String Methods

```python
text = "data science"
print(text.upper())      # DATA SCIENCE
print(text.capitalize()) # Data science
print(text.split())      # ['data', 'science']
```

---

## 📝 Notes

- This file is intended for quick reference while working on projects or reviewing concepts.
- This file contains basic topics in python. 

