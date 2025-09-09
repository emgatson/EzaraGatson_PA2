**************PROGRAMMING ASSIGNMENT 2**************
# 1. NORMALIZATION PROBLEM - Normalization is one of the most basic preprocessing techniques in data analytics. This involves centering and scaling process. Centering means subtracting the data from the mean and scaling means dividing with its standard deviation. 

import numpy as np       //importing numpy

x = np.random.random([5,5])    // Generating a 5x5 matrix of random numbers

y = x.mean()     // Computing for the mean average of all the elements in the matrix

z = x.std()     // Computing for the standard deviation of all the elements in the matrix

norm = (x-y)/z    // Normalize the matrix

print(norm)      // Print the normalized matrix

# 2. DIVISIBLE BY 3 PROBLEM: Create the following 10 x 10 ndarray, which are the squares of the first 100 positive integers.

A = np.arange(1, 101).reshape(10, 10)**2  // Creating a 10x10 array of squares 1-100

div_by_3 = A[A % 3 == 0]   // Get elements divisible by 3

print("Array of squares: \n", A)   // Print array of squares

print("\nElements divisible by 3: \n", div_by_3) // Print elements divisible by 3

print("\nNumber of elements divisible by 3:", div_by_3.size)   // Count how many number of elements is divisible by 3
