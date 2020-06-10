---
layout: default
parent: Statistics
title: Statistical Tests
nav_order: 6

---
# Statistical Tests
___

&nbsp;

**Parametric Test** : used for normally distributed data (`assess group means`)

**Non-Parametric Test** : used for skewed data (`assess group medians`)

&nbsp;

One Tailed : uni-directional (typing speed increases with more typing) <br>
Two tailed: bi-directional (typing speed can increase or decrease with more typing)

&nbsp;

**P-value is the probability of the sample means coming up equal to or even further away from the hypothesized population mean.**

&nbsp;

## **z-Test** (sample size > 30)
Statistical calculation used to compare sample mean to population mean. Most useful `when standard deviation and the sample size is known`.
_The z score tells how far, in standard deviations, a data-point is from the mean._

&nbsp;
## **t-Test** (all sample size _(also referred as sample size < 30)_)
To determine if there is a statistically significant difference between two sample group means. Used **when population standard deviation is unknown.**
The t-score is a ratio between the difference between the two groups and the difference within the groups

_(A large t-score tells you that the groups are different. A small t-score tells you that the groups are similar)_

**- Paired samples t-Test** is used when there is a before - after ideology (matched) <br>
**- Independent samples t-Test (Equal Variances/Unequal Variances)** is also known as a regular t-Test

&nbsp;
## **ANOVA**
It is basically an extension to t test used when more than 2 samples are to be compared.
It is used to determine whether there are any statistically significant differences between the means of three or more independent groups.
ANOVA uses categorical independent variables and a continuous dependent variable

_H0 : all the means of the groups are NOT statistically different (All samples are from the same population)_
_HA : at least two group means are statistically different from each other. (At least one sample comes from a different population)_
_F = (Between Group Variability) ÷ (Within Group Variability)_

&nbsp;
## **Chi-square**
To test dependency or independency of categorical variables. Are 2 categorical variables independent
Anuj says it checks the difference in means + variance
Observed vs expected

&nbsp;
## **F test**
It's a significance of variance test used for model evaluation. It is a one way ANOVA.
It is basically the ratio of 2 chi square tests.

&nbsp;
&nbsp;


| --- | --- | --- | --- |
|  |  | Unmatched | Matched |
| Continuous Data | 2 Groups | t - Test | Paired t - Test |
| > 2 Groups | ANOVA | Blocked Anova |
| Ordinal Data | 2 Groups | Mann-Whitney U or Median Test | Wilcoxon matched pairs or signed ranks test |
| > 2 Groups | Kruskal-Wallis 1-way Anova | Friedman 2-way Anov |
| Nominal Data | 2 Groups | Fisher’s Exact Test | McNemar’s Test |
| > 2 Groups | Chi-square |  |

| --- | --- |
| Type of Test: | Use: |
| Correlational | These tests look for an association between variables |
| Pearson correlation | Tests for the strength of the association between two continuous variables |
| Spearman correlation | Tests for the strength of the association between two ordinal variables (does not rely on the assumption of normal distributed data) |
| Chi-square | Tests for the strength of the association between two categorical variables |
| Comparison of Means: look for the difference between the means of variables |
| Paired T-test | Tests for difference between two related variables |
| Independent T-test | Tests for difference between two independent variables |
| ANOVA | Tests the difference between group means after any other variance in the outcome variable is accounted for |
| Regression: assess if change in one variable predicts change in another variable |
| Simple regression | Tests how change in the predictor variable predicts the level of change in the outcome variable |
| Multiple regression | Tests how change in the combination of two or more predictor variables predict the level of change in the outcome variable |
| Non-parametric: are used when the data does not meet assumptions required for parametric tests |
| Wilcoxon rank-sum test | Tests for difference between two independent variables - takes into account magnitude and direction of difference |
| Wilcoxon sign-rank test | Tests for difference between two related variables - takes into account magnitude and direction of difference |
| Sign test | Tests if two related variables are different – ignores magnitude of change, only takes into account direction |

[When to use what test](http://www.csun.edu/\~amarenco/Fcs%20682/When%20to%20use%20what%20test.pdf)

[Cheatsheet Python tests](https://machinelearningmastery.com/statistical-hypothesis-tests-in-python-cheat-sheet/)
