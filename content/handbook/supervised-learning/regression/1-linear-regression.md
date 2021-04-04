---
title: Linear Regression
date: 2020-01-30T00:38:25.000+09:00
description: Linear Regression
weight: 1

---
# Linear Regression

Linear Regression is the most basic type of regression that there is. It takes a variable and states that on the basis of other variables, it will predict the concerned variable. It does this by simply drawing a line through the points and generating an equation.

`Method = Ordinary Least Square`

***

Dependent Variable (the one you need to predict) **Y  = Continuous**  
Independent Variable (the others with which you will predict) **X = Continuous**  
`i.e the complete data should be numerical in nature`

> The objective is to minimize the sum of squares of the residuals  
> _(residual=difference between observation and the fitted line)_

### Assumptions

1. **Linear relationship** between dependent & independent variables
2. **No presence of outliers**
3. **Independent variables are independent** of each other (non colinear)
4. **Errors,** also called **residuals**
   1. Should have **constant variance** (homoscedasticity)
   2. Are independent and identically distributed (iid) ie **No Autocorrelation**
   3. Are **normally distributed** with a mean of 0

### Tests for Assumptions:

#### Linearity

* Methods :
  * Residuals vs Predicted plot / Residuals vs Actuals plot
* Corrections :
  * Log transformation for strictly positive variables
  * Adding regressor which is non-linear function eg x and x2
  * Create new variable which is sum/product of A & B

#### Multicollinearity

* Methods:
  * Correlation Matrix
  * VIF (Variance Inflation Factor)

> VIF is calculated only on the Independent variables. It runs a series of auxiliary regressions which fetches the R2 value of Xi against other IVs.
> _Eg : If X2, X3, X4, have high R2 value when regressed against X1, it essentially means that X2, X3, X4 can explain a high amount of variation in X1 and it is redundant._ _Range = 1 to ∞ 1 < low < 5 < medium < 10 < high_

#### Homoscedasticity

* Methods:
  * Goldfeld-Quandt test
  * Scatter plot (residuals vs predicted)
* Corrections :
  * Take actual or predicted values of DV and plot it against errors. The plot should be random. If there is a trend, take log of DV.

#### Autocorrelation

* Durbin-Watson Test : Tests for serial correlations between errors
  _Range : 0-4 positive < 2 (uncorrelated) < negative_

#### Multivariate Normal

* Methods:
  * Kolmogorov-Smirnov test / Shapiro-Wilk / Anderson-Darling / Jarque-Bera
  * Q-Q Plot
  * Histogram with fitted normal curve
* Corrections:
  * Nonlinear / Log transformation

### Implementation

    from 

### Outputs and Validation

* R-squared: The most common validation check
* Adjusted R-squared

### One Hot Encoding

This method is used to convert Categorical variables to Continuous variables. It is very simple:

| Transport | >>> | Car | Bus | Train |
| :---: | :---: | :---: | :---: | :---: |
| Car | >>> | 1 | 0 | 0 |
| Bus | >>> | 0 | 1 | 0 |
| Train | >>> | 0 | 0 | 1 |

### Dummy Variable Trap

Lookout for this when converting categorical variables to continuous variables by one hot encoding (flag variable)

* \[x\] Include one less variable when adding dummy variables to regression.
* \[x\] The excluded variable serves as the base variable.
* \[x\] All the other values are a reference to the base variable.