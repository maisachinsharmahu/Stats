# Exercise 6: Plotting Functions and Derivatives (Scilab)

### Objective
To plot a mathematical function and its first derivative on the same graph using Scilab.

### Scilab Code
```scilab
// Define the range for x
x = -5:0.1:5;

// Define the function f(x) = x^2 + 2x + 1
y = x.^2 + 2*x + 1;

// Define the derivative f'(x) = 2x + 2
dy = 2*x + 2;

// Plotting
plot(x, y, "blue"); // Original function
plot(x, dy, "red--"); // Derivative (dashed red line)

// Formatting
title("Function and its Derivative");
xlabel("x");
ylabel("f(x) / f''(x)");
legend("f(x)", "f''(x)");
grid();
```

### Steps to Run
1. Write the script in the Scilab Editor (SciNotes).
2. Save and Execute.
3. The graphics window will pop up with the generated plot.

### Expected Output Plot
![Function Plot](../outputs/06_function_plot.png)
