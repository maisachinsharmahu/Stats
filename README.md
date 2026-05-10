# Advanced Statistics and Computational Mathematics Portfolio

This repository contains 14 comprehensive exercises implemented in Scilab, SPSS, and R. Each exercise is designed to cover the core theoretical concepts and practical applications required for advanced data analysis and mathematical modeling.

---

## 1. Basic Matrix Operations (Scilab)
### Theoretical Background
Matrices are rectangular arrays of numbers arranged in rows and columns. In Scilab, matrix operations are fundamental. 
- **Matrix Addition/Subtraction**: Performed element-wise on matrices of the same dimensions.
- **Matrix Multiplication**: A dot product operation where the number of columns in the first matrix must match the number of rows in the second.
- **Transpose**: An operation that flips a matrix over its diagonal, switching row and column indices.

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

---

## 2. Eigenvalues and Eigenvectors (Scilab)
### Theoretical Background
Eigenvalues and eigenvectors are properties of square matrices. For a square matrix $A$, an eigenvector $v$ and its corresponding eigenvalue $\lambda$ satisfy the equation $Av = \lambda v$. 
- **Physical Significance**: They are used in stability analysis, vibration modeling, and Principal Component Analysis (PCA).
- **Characteristic Equation**: Found by solving $det(A - \lambda I) = 0$.

### Scilab Code
```scilab
A = [1, 2, 3; 4, 5, 6; 7, 8, 9]
[v, d] = spec(A)
disp("Eigenvectors Matrix (v):", v)
disp("Eigenvalues (Diagonal d):", d)
```

---

## 3. Equation Solvers (Scilab)
### Theoretical Background
Solving systems of linear equations ($Ax = b$) is a core task in numerical analysis.
- **Gauss Elimination**: A direct method that transforms the matrix into upper triangular form.
- **Gauss-Jordan**: An extension that transforms the matrix into Reduced Row Echelon Form (RREF).
- **Gauss-Seidel**: An iterative method used for large, sparse systems where convergence is guaranteed if the matrix is diagonally dominant.

### Scilab Code
```scilab
A = [2, 1, -1; -3, -1, 2; -2, 1, 2]
b = [8; -11; -3]
Aug = [A b]
X = rref(Aug)
disp("Solved Matrix (Gauss Jordan):", X)
```

---

## 4. Matrix Properties (Scilab)
### Theoretical Background
Matrix algebra follows specific laws:
- **Commutative (Addition)**: $A + B = B + A$.
- **Associative**: $(A + B) + C = A + (B + C)$ and $(AB)C = A(BC)$.
- **Distributive**: $A(B + C) = AB + AC$.
- **Note**: Matrix multiplication is generally **not** commutative ($AB \neq BA$).

### Scilab Code
```scilab
A = [1, 2; 3, 4]; B = [5, 6; 7, 8]; C = [9, 1; 2, 3]
disp("Commutative (A+B == B+A):", (A + B) == (B + A))
disp("Associative ((A*B)*C == A*(B*C)):", ((A * B) * C) == (A * (B * C)))
disp("Distributive (A*(B+C) == AB + AC):", (A * (B + C)) == ((A * B) + (A * C)))
```

---

## 5. Reduced Row Echelon Form (Scilab)
### Theoretical Background
The Reduced Row Echelon Form (RREF) is a standardized form of a matrix reached through elementary row operations.
- **Conditions**: The first non-zero entry in each row is 1 (pivot), and each pivot is the only non-zero entry in its column.
- **Applications**: Determining the rank of a matrix and the consistency of linear systems.

### Scilab Code
```scilab
A = [1, 2, 3, 4; 5, 6, 7, 8; 9, 10, 11, 12]
R = rref(A)
disp("Matrix in RREF:", R)
```

---

## 6. Plotting Functions and Derivatives (Scilab)
### Theoretical Background
Graphical representation helps in understanding the behavior of functions and their rates of change.
- **Function**: A relationship where each input has a unique output.
- **Derivative**: Represents the instantaneous rate of change or the slope of the tangent at any point on the function.
- **Scilab Plotting**: Uses the `plot()` function with customizable colors and line styles.

### Scilab Code
```scilab
x = -5:0.1:5;
y = x.^2 + 2*x + 1;
dy = 2*x + 2;
plot(x, y, "blue"); plot(x, dy, "red--");
title("Function and its Derivative");
legend("f(x)", "f'(x)");
grid();
```
<img src="./outputs/06_function_plot.png" width="500">

---

## 7. Frequency Table (SPSS)
### Theoretical Background
Frequency distribution is a summary of data showing the count of occurrences in each category or interval.
- **Absolute Frequency**: Actual count.
- **Relative Frequency**: Proportion of total count.
- **Cumulative Frequency**: Sum of frequencies up to the current interval.

### Steps in SPSS
1. Navigate to `Analyze` -> `Descriptive Statistics` -> `Frequencies`.
2. Select the variables and ensure "Display frequency tables" is checked.

| Category | Frequency | Percent | Valid Percent | Cumulative Percent |
|----------|-----------|---------|---------------|--------------------|
| Group A  | 10        | 50.0    | 50.0          | 50.0               |
| Group B  | 10        | 50.0    | 50.0          | 100.0              |

---

## 8. Finding Outliers (SPSS)
### Theoretical Background
Outliers are data points that deviate significantly from the rest of the dataset.
- **Identification**: Commonly found using the Interquartile Range (IQR) method. Any point below $Q1 - 1.5 \times IQR$ or above $Q3 + 1.5 \times IQR$ is an outlier.
- **Impact**: Outliers can skew results, especially the mean and standard deviation.

### Steps in SPSS
1. `Analyze` -> `Descriptive Statistics` -> `Explore`.
2. Move variable to `Dependent List` -> `Plots` -> Select `Boxplots`.
3. SPSS will identify outliers with labels in the boxplot output.

---

## 9. Risk Analysis of Projects (SPSS)
### Theoretical Background
In financial statistics, risk is the uncertainty of returns.
- **Standard Deviation ($\sigma$)**: Measures absolute risk.
- **Coefficient of Variation (CV)**: Measures relative risk ($CV = \sigma / \mu$). It is useful when comparing projects with different mean returns.
- **Rule**: Higher CV indicates higher risk per unit of return.

### Example Metrics
| Project | Mean Return | Std. Deviation | CV | Risk Rank |
|---------|-------------|----------------|----|-----------|
| A       | 10%         | 2%             | 0.2| Low       |
| B       | 12%         | 6%             | 0.5| High      |

---

## 10. Scatter Plots and Diagnostics (R)
### Theoretical Background
Regression diagnostics verify if the assumptions of linear regression hold.
- **Scatter Plot**: Shows the relationship between two continuous variables.
- **Residuals vs Fitted**: Checks for homoscedasticity (constant variance).
- **Leverage**: Identifies observations that have a great influence on the model's coefficients.

### R Code
```r
model <- lm(mpg ~ hp + wt, data = mtcars)
par(mfrow=c(2,2)) # diagnostic grid
plot(model)
```
<img src="./outputs/10_r_plots.png" width="500">

---

## 11. Correlation Analysis (R)
### Theoretical Background
Correlation quantifies the relationship between two variables.
- **Pearson Coefficient ($r$)**: Ranges from -1 to +1.
- **Significance ($p$-value)**: Determines if the observed correlation is statistically significant ($p < 0.05$).

### R Code
```r
x <- c(12, 15, 18, 20, 25, 30); y <- c(10, 14, 17, 22, 24, 28)
cor_value <- cor(x, y)
cor_test <- cor.test(x, y)
print(cor_value)
```

---

## 12. Time Series Analysis (R)
### Theoretical Background
A time series is a sequence of data points indexed in time order.
- **Components**: Trend (long-term movement), Seasonality (repeating patterns), and Noise.
- **Stationarity**: A property where statistical characteristics like mean and variance are constant over time.

### R Code
```r
sales_ts <- ts(c(350, 440, 460, 530, 520, 540, 680, 590, 480, 510, 380, 450), 
               start=c(2018, 1), frequency=12)
plot(sales_ts, col="darkblue", lwd=2, main="Time Series Pattern")
```
<img src="./outputs/12_r_timeseries.png" width="500">

---

## 13. Linear Regression (R)
### Theoretical Background
Linear regression models the relationship between a scalar response and one or more explanatory variables.
- **Model**: $Y = \beta_0 + \beta_1 X + \epsilon$
- **R-squared**: Explains the goodness of fit (how well the model explains the data).

### R Code
```r
model <- lm(mpg ~ wt, data = mtcars)
summary(model)
plot(mtcars$wt, mtcars$mpg)
abline(model, col="red", lwd=2)
```

---

## 14. Probability and Distributions (R)
### Theoretical Background
Probability distributions describe the likelihood of outcomes.
- **Normal Distribution**: A symmetric, bell-shaped curve defined by mean ($\mu$) and standard deviation ($\sigma$).
- **PDF**: The Probability Density Function defines the shape of the curve.
- **Area under Curve**: Total area is 1, representing 100% probability.

### R Code
```r
x <- seq(-4, 4, length=100); y <- dnorm(x, mean=0, sd=1)
plot(x, y, type="l", col="black", main="Normal PDF")
polygon(c(x, rev(x)), c(y, rep(0, length(y))), col="lightblue")
```
<img src="./outputs/14_r_probability.png" width="500">
