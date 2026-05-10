# Exercise 5: Reduced Row Echelon Form (Scilab)

### Objective
To transform a matrix into its Reduced Row Echelon Form (RREF) using elementary row operations.

### Scilab Code
```scilab
// Define a matrix
A = [1, 2, 3, 4; 5, 6, 7, 8; 9, 10, 11, 12]

// Find RREF
R = rref(A)

disp("Original Matrix A:", A)
disp("Reduced Row Echelon Form (RREF):", R)
```

### Explanation
The `rref()` function in Scilab uses the Gauss-Jordan elimination algorithm to reduce the matrix. It is extremely useful for solving systems of linear equations and finding the rank of a matrix.

### Expected Output
```text
 Reduced Row Echelon Form (RREF):
    1.   0.  -1.  -2.
    0.   1.   2.   3.
    0.   0.   0.   0.
```
