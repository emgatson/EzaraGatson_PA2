# **GATSON_EMR_PA2**

# **ECE Programming Assignment 2**
## **PROBLEM 1**
A program that generates a random 5×5 matrix, computes the mean and standard deviation of all its elements, and then normalizes the matrix.

---
The function np.random.random([5,5]) creates an array of size 5×5 with each element being a random floating-point number between 0 and 1.
```python
import numpy as np            # Imports the NumPy library for numerical operations
x = np.random.random([5, 5])  # Creates a 5x5 matrix with random values between 0 and 1
```

The .mean() method calculates the overall average value of the matrix x, and the .std() method computes how spread out the values are from the mean.
```python
y = x.mean()                  # Computes the mean (average) of all elements in x
z = x.std()                   # Computes the standard deviation of all elements in x
```

Each element of x is first centered by subtracting the mean y and then scaled by dividing by the standard deviation z. The resulting array norm has a mean of approximately 0 and a standard deviation of approximately 1. Then prints the statements
```python
norm = (x - y) / z            # Normalizes the matrix

print("Original matrix:\n", x)   # Displays the original 5x5 matrix
print("\nMean of all elements:", y)   # Displays the computed mean
print("Standard deviation of all elements:", z)  # Displays the computed standard deviation
print("\nNormalized matrix:\n", norm)   # Displays the normalized matrix
```

## **PROBLEM 2**
A program that generates a 10×10 matrix of the squares of the first 100 integers and selects the elements divisible by 3.

---

The function np.arange(1,101) generates numbers from 1 to 100, .reshape(10,10) arranges them into a 10×10 matrix, and **2 squares each element, so the matrix A contains the squares of the numbers 1 to 100.
```python
import numpy as np            # Imports the NumPy library
A = np.arange(1, 101).reshape(10, 10) ** 2   # Creates a 10x10 matrix of squares of the first 100 positive integers
```
The expression A % 3 == 0 creates a boolean mask that is True for elements divisible by 3. Then prints the statment.
```python
div_by_3 = A[A % 3 == 0]      # Selects elements of A that are divisible by 3
print("Array of squares:\n", A)                 # Displays the full 10x10 matrix of squares
print("\nElements divisible by 3:\n", div_by_3)  # Displays the elements divisible by 3
print("\nNumber of elements divisible by 3:", div_by_3.size)   # Displays how many elements are divisible by 3
```
---
-VERSION 2-
