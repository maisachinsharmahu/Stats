# Exercise 14: Probability and Distributions (R)

### Objective
To implement concepts of probability and visualize common distributions like the Normal Distribution using R.

### R Code
```r
# 1. Normal Distribution Plot
x <- seq(-4, 4, length=100)
y <- dnorm(x, mean=0, sd=1)

plot(x, y, type="l", lwd=2, col="black", 
     main="Standard Normal Distribution", 
     xlab="z-score", ylab="Density")
polygon(c(x, rev(x)), c(y, rep(0, length(y))), col="lightblue")

# 2. Calculating Probabilities
# Probability that X < 1.96 (for Standard Normal)
prob <- pnorm(1.96)
print(paste("Probability (Z < 1.96):", prob))

# Generating Random Numbers from Normal Distribution
random_nums <- rnorm(10, mean=50, sd=5)
print(random_nums)
```

### Key Functions
- `dnorm()`: Density function of the Normal Distribution.
- `pnorm()`: Cumulative distribution function (CDF).
- `rnorm()`: Generates random deviates.

### Expected Output Plot
![Normal Distribution](../outputs/14_r_probability.png)
