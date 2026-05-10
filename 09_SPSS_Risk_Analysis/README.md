# Exercise 9: Risk Analysis of Projects (SPSS)

### Objective
To determine which of two mutually exclusive projects is riskier based on their expected returns and variability.

### Concept
Risk is measured by the **Coefficient of Variation (CV)**:
`CV = (Standard Deviation / Mean) * 100`

### Steps in SPSS
1. **Data Entry**: Create two variables `Project_A` and `Project_B` with their projected annual returns.
2. **Analyze**: Go to `Analyze` -> `Descriptive Statistics` -> `Descriptives`.
3. **Selection**: Move both projects to the `Variable(s)` list.
4. **Options**: Click `Options` and ensure `Mean` and `Std. deviation` are checked.
5. **Calculate CV**: Manually compute CV using the output table values.

### Decision Rule
- The project with the **higher Coefficient of Variation** is considered the **more risky** project.
- If Means are same, the one with higher **Standard Deviation** is riskier.

### Example Output
| Project | Mean | Std. Deviation | CV (Calculated) | Risk Level |
|---------|------|----------------|-----------------|------------|
| A       | 15%  | 3%             | 20%             | Lower      |
| B       | 15%  | 6%             | 40%             | **Higher** |
