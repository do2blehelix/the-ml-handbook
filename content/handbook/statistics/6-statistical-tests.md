---
layout: default
parent: Statistics
title: Statistical Tests
nav_order: 6
has_children: false

---
# Statistical Tests
Statistical tests are conducted to accept or reject hypothesis. They can be divided into tests catering to specific distributions of data.


- **Parametric Test** : used for normally distributed data (`assess group means`)  
- **Non-Parametric Test** : used for skewed data (`assess group medians`)

The tests are also classified according to their tails.
- One Tailed : uni-directional (typing speed increases with more typing) <br>
- Two tailed: bi-directional (typing speed can increase or decrease with more typing)

⚠ **P-value is the probability of the sample means coming up equal to or even further away from the hypothesized population mean.**

### **z-Test** (sample size > 30)

Statistical calculation used to compare sample mean to population mean. 
Most useful when **standard deviation and the sample size is known**.

> _The z score tells how far, in standard deviations, a data-point is from the mean._

### **t-Test** (all sample size _also referred as sample size < 30_ )

To determine if there is a statistically significant difference between two sample group means.
Used **when population standard deviation is unknown.**

> The t-score is a ratio between the difference between the two groups and the difference within the groups

_(A large t-score tells you that the groups are different. A small t-score tells you that the groups are similar)_

**- Paired samples t-Test** is used when there is a before - after ideology (matched)
**- Independent samples t-Test (Equal Variances/Unequal Variances)** is also known as a regular t-Test

### **ANOVA**

It is basically an extension to t test used when more than 2 samples are to be compared.
It is used to determine whether there are any **statistically significant differences between the means of three or more independent groups**.
ANOVA uses categorical independent variables and a continuous dependent variable

_`H0` : all the means of the groups are NOT statistically different (All samples are from the same population)_
_`HA` : at least two group means are statistically different from each other. (At least one sample comes from a different population)_
_`F` = (Between Group Variability) ÷ (Within Group Variability)_

### **Chi-square**

To test dependency or independency of categorical variables. Are 2 categorical variables independent
Anuj says it checks the difference in means + variance
Observed vs expected

### **F test**

It's a significance of variance test used for model evaluation. It is a one way ANOVA.
It is basically the ratio of 2 chi square tests.

&nbsp;

---

| [When to use what test](http://www.csun.edu/\~amarenco/Fcs%20682/When%20to%20use%20what%20test.pdf) | [Cheatsheet Python tests](https://machinelearningmastery.com/statistical-hypothesis-tests-in-python-cheat-sheet/) |