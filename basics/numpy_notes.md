# 📌 NumPy Notes for Data Science
This file contains brief introduction and code examples about NumPy.
Numpy is a python library used for numerical computation in python.
---

## 🔹 Importing NumPy

```python
import numpy as np
```

---

## 🔹 Creating Arrays

```python
arr = np.array([1, 2, 3])
zeros = np.zeros((2, 3)) #creating array filled with zeros
ones = np.ones((3, 3)) # #creating array filled with ones
identity = np.eye(4) #creating identity matrix
arange = np.arange(0, 10, 2) # Creating an array from 0 to 10 (exclusive) with step size of 2
#array([0, 2, 4, 6, 8]) 
linspace = np.linspace(0, 1, 5) ## Creating an array of 5 equally spaced values between 0 and 1
#array([0.  , 0.25, 0.5 , 0.75, 1.  ])
```

---

## 🔹 Array Properties

```python
arr.shape       # (3,)
arr.ndim        # number of dimensions
arr.dtype       # data type
arr.size        # total number of elements
```

---

## 🔹 Indexing & Slicing

```python
a = np.array([[1, 2, 3], [4, 5, 6]])
a[0, 1]      # 2
a[:, 1]      # second column
a[1, :]      # second row
```

---

## 🔹 Array Operations

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

a + b         # [5 7 9]
a * 2         # [2 4 6]
a ** 2        # [1 4 9]
np.dot(a, b)  # 32 (dot product)
```

---

## 🔹 Useful Functions

```python
np.mean(a)
np.std(a)
np.min(a)
np.max(a)
np.sum(a)
np.sort(a)
```

---

## 🔹 Reshaping Arrays

```python
a = np.array([[1, 2], [3, 4], [5, 6]])
a.reshape((2, 3))
a.flatten()  # converts to 1D
```

---

## 🔹 Random Numbers

```python
np.random.seed(42)           # for reproducibility
np.random.rand(3, 2)         # random floats in [0,1)
np.random.randint(0, 10, 5)  # random integers
```

---

## 📌 Notes

- NumPy is highly efficient and forms the base for most ML libraries.
- Practice slicing and broadcasting to improve fluency.
- Check: `numpy-pandas.ipynb` for applied examples.

---
