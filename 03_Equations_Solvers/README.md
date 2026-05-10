# Exercise 3: Equation Solvers (Scilab)

### Objective
To solve systems of linear equations using Gauss Elimination, Gauss Jordan, and Gauss Seidel methods.

### 1. Gauss Elimination / Gauss Jordan
```scilab
// Augmented matrix [A|b]
A = [2, 1, -1; -3, -1, 2; -2, 1, 2]
b = [8; -11; -3]
Aug = [A b]

// Solving using rref (Reduced Row Echelon Form) which implements Gauss Jordan
X = rref(Aug)
disp("Solved Matrix (Gauss Jordan):", X)
```

### 2. Gauss Seidel (Iterative Method)
```scilab
// Example for a 2x2 system
A = [4, 1; 1, 3]
b = [7; 8]
x = [0; 0] // initial guess

for i = 1:10
    x(1) = (b(1) - A(1,2)*x(2)) / A(1,1)
    x(2) = (b(2) - A(2,1)*x(1)) / A(2,2)
end
disp("Gauss Seidel Result after 10 iterations:", x)
```

### Expected Output
```text
 Solved Matrix:
    1.  0.  0.   2.
    0.  1.  0.   3.
    0.  0.  1.  -1.
(Solution: x=2, y=3, z=-1)
```
