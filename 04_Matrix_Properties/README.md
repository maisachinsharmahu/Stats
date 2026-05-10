# Exercise 4: Matrix Properties (Scilab)

### Objective
To verify the fundamental properties of matrices: Associative, Commutative, and Distributive.

### Scilab Code
```scilab
A = [1, 2; 3, 4]
B = [5, 6; 7, 8]
C = [9, 1; 2, 3]

// 1. Commutative Property (Addition: A+B = B+A)
prop1_left = A + B
prop1_right = B + A
disp("Commutative (A+B == B+A):", prop1_left == prop1_right)

// 2. Associative Property (Multiplication: (A*B)*C == A*(B*C))
prop2_left = (A * B) * C
prop2_right = A * (B * C)
disp("Associative ((A*B)*C == A*(B*C)):", prop2_left == prop2_right)

// 3. Distributive Property (A*(B+C) == A*B + A*C)
prop3_left = A * (B + C)
prop3_right = (A * B) + (A * C)
disp("Distributive (A*(B+C) == AB + AC):", prop3_left == prop3_right)
```

### Note
- **Matrix Multiplication is NOT Commutative**: `A * B` is generally not equal to `B * A`.
- Scilab returns a matrix of `T/F` (boolean) for the equality checks.
