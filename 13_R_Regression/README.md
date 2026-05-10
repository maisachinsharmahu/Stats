# Exercise 13: Linear Regression (R)

### Objective
To implement simple linear regression in R to predict a dependent variable based on an independent variable.

### R Code
```r
# Data: Weight of cars vs. Miles per gallon
data(mtcars)

# Linear Regression Model
# formula: y ~ x
model <- lm(mpg ~ wt, data = mtcars)

# Display Summary (Intercept, Coefficients, R-squared)
summary(model)

# Plotting
plot(mtcars$wt, mtcars$mpg, main="Regression: Weight vs MPG",
     xlab="Weight (1000 lbs)", ylab="Miles/Gallon")
abline(model, col="red", lwd=2)
```

### Key Output Metrics
- **Intercept**: The value of y when x = 0.
- **Estimate (Slope)**: The rate of change of y with respect to x.
- **R-squared**: The proportion of variance in y explained by x.

### Expected Summary Output
```text
Coefficients:
            Estimate Std. Error t value Pr(>|t|)    
(Intercept)  37.2851     1.8776  19.858  < 2e-16 ***
wt           -5.3445     0.5591  -9.559 1.29e-10 ***

Multiple R-squared:  0.7528
```
