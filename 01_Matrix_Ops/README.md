# Exercise 1: Basic Matrix Operations (Scilab)

### Objective
To implement basic operations like addition, subtraction, multiplication, and transpose on matrices using Scilab.

### Scilab Code
```scilab
// Define two matrices
A = [1, 2; 3, 4]
B = [5, 6; 7, 8]

// Matrix Addition
C = A + B

// Matrix Subtraction
D = A - B

// Matrix Multiplication
E = A * B

// Matrix Transpose
F = A'

// Display Results
disp("Matrix A:", A)
disp("Matrix B:", B)
disp("Addition (A+B):", C)
disp("Subtraction (A-B):", D)
disp("Multiplication (A*B):", E)
disp("Transpose of A:", F)
```

### Steps to Run
1. Open Scilab Console.
2. Copy the code into the editor or directly into the console.
3. Press Enter to see the result.

### Expected Output
```text
 Addition (A+B):
    6.    8.
    10.   12.

 Subtraction (A-B):
   -4.   -4.
   -4.   -4.

 Multiplication (A*B):
    19.   22.
    43.   50.
```
