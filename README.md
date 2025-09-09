# AdrianTiu30-2nd_Programming_Assignment-2ECE-A-

# Programming Assignment 2

This repository presents the explanation of my submitted code for 
**ECE2112: Advanced Computer Programming and Algorithm**.

## 1. Normalization Problem
**Goal:** Generate a random 5x5 array, calculate its mean and standard deviation, normalize the array, and save it as a file.

**Process:**
1. A random 5x5 array is generated with values between 0 and 1.
2. The mean and standard deviation of the array are calculated.
3. The original array, mean, standard deviation, and normalized array are printed.
4. The normalized array is saved as a "X_normalized.npy" file.

**Step-by-step:**
1. Generate a random 5x5 array.
2. Compute the mean and standard deviation.
3. Normalize the array.
4. Print results (original array, mean, std, normalized array).
5. Save the normalized array as **"X_normalized.npy"**.

## Code Snippet:
```
import numpy as np

# Create random 5x5 array and populate with numbers between 0 and 1
X = np.random.rand(5, 5)

# Calculate mean and standard deviation
mean = X.mean()
std = X.std()

# Normalize array 
X_normalized = (X - mean) / std

# Print original array and normalized array
print("Original Array:\n", X)
print("\nMean of X:", mean_X)
print("Standard Deviation of X:", std_X)
print("\nNormalized Array:\n", X_normalized)

# Save and print saved file name
np.save("X_normalized.npy", X_normalized)
print("\nNormalized array saved as 'X_normalized.npy'")
```

## 2. Divisible By 3 Problem
