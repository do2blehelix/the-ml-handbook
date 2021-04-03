---
title: "Covariance & Correlation"
date: 2020-01-30T00:38:25+09:00
description: Covariance & Correlation
weight: 4

---
# Covariance & Correlation

Correlation is a statistical technique that can show whether and how strongly pairs of variables are related. For example, height and weight are related; taller people tend to be heavier than shorter people.


⚠️ Correlation doesn't imply causation



## Covariance :
**Covariance is nothing but a measure of correlation. On the contrary, correlation refers to the scaled form of covariance.**


`Returns a value between -∞ & +∞`  
Sum \[(X-u1) (Y-u2)\] / (n-1)



## Correlation :
**Correlation is the standardized form of covariance.**

`Returns a value between 0 (very weak) & ±1 (very strong), inclusive`


**Multicollinearity** : describes a linear relationship between two or more variables   
**Autocorrelation** : describes correlation of a variable with itself in a time lag


### Pearson Correlation _(Karl Pearson)_

* Measures the strength of linear dependence between two variables
* A correlation of 0 doesn’t imply ‘no relationship’ between the 2 variables, it just implies ‘no linear relationship’
* Calculated as the covariance of X and Y divided by product of standard deviation of X and Y
* Denoted as 𝝆 (rho) for population and **r** for sample correlation coefficient

r = i=1n\[(xi- x) (yi-y)\]i=1n(xi- x)i=1n(yi- y)


### Spearman Correlation

* Is a non-parametric technique.
* Does not test a linear relationship but the strength of monotonicity between 2 variables ie the direction.
* Immune to outliers
* Can detect non-linear monotonic relationships easily as highly correlated.
* Divides the variable observations into ranks and runs correlation analysis based on the ranks instead of the original observation data.

_However, Spearman correlation values tend to be subdued as compared to Pearson’s when detecting linear relationships: due to removal of impact of squared distances_
