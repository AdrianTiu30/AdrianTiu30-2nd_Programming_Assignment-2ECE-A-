# AdrianTiu30-2nd_Programming_Assignment-2ECE-A-

# Programming Assignment 2

This repository presents the explanation of my submitted code for 
**ECE2112: Advanced Computer Programming and Algorithm**.

# Data Preprocessing and Array Manipulation Problems
This project demonstrates Python scripts that use NumPy for basic data preprocessing and numerical computation. The problems include normalization of data and extracting values divisible by 3 from an array of squared integers.

## 1. Normalization Problem
**Task:** Generate a random 5x5 array, calculate its mean and standard deviation, normalize the array, and save it as a file.

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
A random 5×5 NumPy array is generated with values between 0 and 1. The mean and standard deviation of the array are computed using ```.mean()``` and ```.std()```. Each element is normalized by subtracting the mean and dividing by the standard deviation. The original array, mean, standard deviation, and normalized array are printed. The normalized array is saved to a file named ```X_normalized.npy```.

## Result:
```
Original Array:
 [[0.79158877 0.97072807 0.57234803 0.57228944 0.85558708]
 [0.57529736 0.87616537 0.75805133 0.61938184 0.02777545]
 [0.74561539 0.88014924 0.4999412  0.38564106 0.81170992]
 [0.64349905 0.77677405 0.13163767 0.30795296 0.48595209]
 [0.57985414 0.16141154 0.01279278 0.73175834 0.14061613]]

Mean of X: 0.5648285400837969
Standard Deviation of X: 0.2213708549757269

Normalized Array:
 [[ 0.84345774  1.48639927  0.05658978  0.05637949  1.07315146]
 [ 0.06717509  1.14700816  0.72308988  0.22539687 -1.89791341]
 [ 0.67845655  1.16130649 -0.20328264 -0.6135126   0.91567371]
 [ 0.311955    0.79028682 -1.52514574 -0.89233978 -0.25349038]
 [ 0.08352963 -1.41828558 -1.95168707  0.62872279 -1.49292152]]

Normalized array saved as 'X_normalized.npy'
```


## 2. Divisible By 3 Problem

**Task:** Create a 10x10 array of squares of the first 100 positive integers, find elements divisible by 3, and save the result.

## Code Snippet:
```
import numpy as np

# Create 10x10 array of squares of first 100 positive integers
A = np.arange(1, 101)**2
A = A.reshape(10, 10)

# Find elements divisible by 3
div_by_3 = A[A % 3 == 0]

# Save result
np.save("div_by_3.npy", div_by_3)

# Print results
print("Array of squares (10x10):\n", A)
print("\nNumbers divisible by 3:\n", div_by_3)
print("\nResult saved as 'div_by_3.npy'")
```
```np.arange(1, 101)``` generates the numbers 1 to 100. Squaring each value (**2) produces the first 100 square numbers. The array is reshaped into a 10×10 matrix. A condition (A % 3 == 0) is applied to extract only the numbers divisible by 3. The resulting numbers are saved in a file named ```div_by_3.npy```.


## Result:
```
Array of squares (10x10):
 [[    1     4     9    16    25    36    49    64    81   100]
 [  121   144   169   196   225   256   289   324   361   400]
 [  441   484   529   576   625   676   729   784   841   900]
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]

Numbers divisible by 3:
 [   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
 2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
 7569 8100 8649 9216 9801]

Result saved as 'div_by_3.npy'
```
# --Version 2--
