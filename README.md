# Advanced Statistics Practical Portfolio (Scilab, SPSS, R)

This repository contains 14 comprehensive statistical exercises. All details, including code and outputs, are consolidated here for easy reference.

---

## Table of Contents
1. [Basic Matrix Operations (Scilab)](#1-basic-matrix-operations-scilab)
2. [Eigenvalues and Eigenvectors (Scilab)](#2-eigenvalues-and-eigenvectors-scilab)
3. [Equation Solvers (Scilab)](#3-equation-solvers-scilab)
4. [Matrix Properties (Scilab)](#4-matrix-properties-scilab)
5. [Reduced Row Echelon Form (Scilab)](#5-reduced-row-echelon-form-scilab)
6. [Plotting Functions and Derivatives (Scilab)](#6-plotting-functions-and-derivatives-scilab)
7. [Frequency Table (SPSS)](#7-frequency-table-spss)
8. [Finding Outliers (SPSS)](#8-finding-outliers-spss)
9. [Risk Analysis of Projects (SPSS)](#9-risk-analysis-of-projects-spss)
10. [Scatter Plots and Diagnostics (R)](#10-scatter-plots-and-diagnostics-r)
11. [Correlation Analysis (R)](#11-correlation-analysis-r)
12. [Time Series Analysis (R)](#12-time-series-analysis-r)
13. [Linear Regression (R)](#13-linear-regression-r)
14. [Probability and Distributions (R)](#14-probability-and-distributions-r)

---

## 1. Basic Matrix Operations (Scilab)
### Scilab Code
```scilab
A = [1, 2; 3, 4]
B = [5, 6; 7, 8]
C = A + B
D = A - B
E = A * B
F = A'
disp("Addition:", C, "Subtraction:", D, "Multiplication:", E, "Transpose:", F)
```

## 2. Eigenvalues and Eigenvectors (Scilab)
### Scilab Code
```scilab
A = [1, 2, 3; 4, 5, 6; 7, 8, 9]
[v, d] = spec(A)
disp("Eigenvectors:", v, "Eigenvalues:", d)
```

## 3. Equation Solvers (Scilab)
### Scilab Code
```scilab
A = [2, 1, -1; -3, -1, 2; -2, 1, 2]
b = [8; -11; -3]
Aug = [A b]
X = rref(Aug)
disp("Solved Matrix (Gauss Jordan):", X)
```

## 4. Matrix Properties (Scilab)
### Scilab Code
```scilab
A = [1, 2; 3, 4]; B = [5, 6; 7, 8]; C = [9, 1; 2, 3]
disp("Commutative (A+B == B+A):", (A + B) == (B + A))
disp("Associative ((A*B)*C == A*(B*C)):", ((A * B) * C) == (A * (B * C)))
disp("Distributive (A*(B+C) == AB + AC):", (A * (B + C)) == ((A * B) + (A * C)))
```

## 5. Reduced Row Echelon Form (Scilab)
### Scilab Code
```scilab
A = [1, 2, 3, 4; 5, 6, 7, 8; 9, 10, 11, 12]
R = rref(A)
disp("RREF:", R)
```

## 6. Plotting Functions and Derivatives (Scilab)
### Scilab Code
```scilab
x = -5:0.1:5;
y = x.^2 + 2*x + 1;
dy = 2*x + 2;
plot(x, y, "blue"); plot(x, dy, "red--");
title("Function and its Derivative");
legend("f(x)", "f'(x)");
```
![Function Plot](./outputs/06_function_plot.png)

## 7. Frequency Table (SPSS)
### Steps
1. `Analyze` -> `Descriptive Statistics` -> `Frequencies`.
2. Select variables and click `OK`.

| Age | Frequency | Percent | Valid Percent | Cumulative Percent |
|-----|-----------|---------|---------------|--------------------|
| 18  | 5         | 25.0    | 25.0          | 25.0               |
| Total | 20      | 100.0   | 100.0         |                    |

## 8. Finding Outliers (SPSS)
### Steps
1. `Analyze` -> `Descriptive Statistics` -> `Explore`.
2. Move variable to `Dependent List` -> `Plots` -> `Boxplots`.

## 9. Risk Analysis of Projects (SPSS)
### Concept
`CV = (Standard Deviation / Mean) * 100`. The higher CV project is riskier.

## 10. Scatter Plots and Diagnostics (R)
### R Code
```r
model <- lm(mpg ~ hp + wt, data = mtcars)
par(mfrow=c(2,2))
plot(model)
```
![R Diagnostics](./outputs/10_r_plots.png)

## 11. Correlation Analysis (R)
### R Code
```r
x <- c(12, 15, 18, 20, 25, 30); y <- c(10, 14, 17, 22, 24, 28)
cor(x, y)
```

## 12. Time Series Analysis (R)
### R Code
```r
sales_ts <- ts(c(350, 440, 460, 530, 520, 540, 680, 590, 480, 510, 380, 450), start=c(2018, 1), frequency=12)
plot(sales_ts, col="blue", lwd=2)
```
![R Time Series](./outputs/12_r_timeseries.png)

## 13. Linear Regression (R)
### R Code
```r
model <- lm(mpg ~ wt, data = mtcars)
summary(model)
plot(mtcars$wt, mtcars$mpg)
abline(model, col="red")
```

## 14. Probability and Distributions (R)
### R Code
```r
x <- seq(-4, 4, length=100); y <- dnorm(x, mean=0, sd=1)
plot(x, y, type="l", col="black")
polygon(c(x, rev(x)), c(y, rep(0, length(y))), col="lightblue")
```
![Normal Distribution](./outputs/14_r_probability.png)

---
**Good luck with the Exams! 🚀**
