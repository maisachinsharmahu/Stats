# Exercise 2: Eigenvalues and Eigenvectors (Scilab)

### Objective
To calculate the eigenvalues and eigenvectors of a given square matrix using Scilab's built-in functions.

### Scilab Code
```scilab
// Define a square matrix
A = [1, 2, 3; 4, 5, 6; 7, 8, 9]

// Find eigenvalues and eigenvectors
// [v, d] = spec(A) where v is eigenvectors and d is diagonal matrix of eigenvalues
[v, d] = spec(A)

disp("Matrix A:", A)
disp("Eigenvectors (v):", v)
disp("Eigenvalues (Diagonal d):", d)
```

### Key Functions
- `spec(A)`: Returns the spectral decomposition (eigenvalues and eigenvectors) of matrix A.

### Expected Output
```text
 Eigenvalues:
    16.116844
   -1.116844
    0.

 Eigenvectors:
   -0.2319707  -0.785834   0.4082483
   -0.5253221  -0.0867513 -0.8164966
   -0.8186735   0.6123313  0.4082483
```
