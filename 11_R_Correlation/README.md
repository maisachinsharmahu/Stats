# Exercise 11: Correlation Analysis (R)

### Objective
To calculate the correlation coefficient between two variables to determine the strength and direction of their relationship.

### R Code
```r
# Define two vectors
x <- c(12, 15, 18, 20, 25, 30)
y <- c(10, 14, 17, 22, 24, 28)

# Calculate Pearson Correlation
correlation <- cor(x, y)

# Significance test
test <- cor.test(x, y)

print(paste("Correlation Coefficient:", correlation))
print(test)
```

### Interpretation
- **Value near +1**: Strong Positive Correlation.
- **Value near -1**: Strong Negative Correlation.
- **Value near 0**: No Linear Correlation.

### Expected Output
```text
[1] "Correlation Coefficient: 0.9897"

	Pearson's product-moment correlation
data:  x and y
t = 13.84, df = 4, p-value = 0.00016
```
