# Exercise 10: Scatter Plots and Diagnostics (R)

### Objective
To draw scatter diagrams, analyze residual plots, and identify outliers and influential data points using R.

### R Code
```r
# Load data (using built-in mtcars as example)
data(mtcars)

# Linear Regression Model
model <- lm(mpg ~ hp + wt, data = mtcars)

# 1. Scatter Diagram with Regression Line
plot(mtcars$hp, mtcars$mpg, main="Scatter Plot", xlab="Horsepower", ylab="MPG")
abline(model, col="red")

# 2. Residuals, Outliers, and Influential Data
# This single command generates 4 diagnostic plots
par(mfrow=c(2,2)) # Arrange plots in 2x2 grid
plot(model)
```

### Explanation of Plots
- **Residuals vs Fitted**: Checks for non-linearity.
- **Normal Q-Q**: Checks if residuals are normally distributed.
- **Scale-Location**: Checks for homoscedasticity (constant variance).
- **Residuals vs Leverage**: Identifies influential cases (high leverage) using Cook's distance.

### Expected Output Plot
![R Diagnostics](../outputs/10_r_plots.png)
