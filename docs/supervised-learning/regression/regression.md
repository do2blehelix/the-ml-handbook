---
layout: default
has_children: true
title: Regression
parent: Supervised Learning
nav_order: 1

---
## Regression

Regression analysis is a statistical process for estimating the relationships among variables.

Correlation only measures the strength of a linear relationship, it doesn’t tell anything regarding the relationship. Regression is used to figure out the relationship itself.

_Eg: if correlation between Y and X is 0.7 then it says if X increases, 70% of the time Y increases. But regression tells if X increases by 1 unit, by how many units does Y increase._

**Types of Data**

* Cross-sectional : data at a single point in time with multiple variables
* Time Series : data at multiple points in time with a single variable
* Longitudinal / Pooled / Panel : cross sectional time series data

**B-coefficient** : if X increases by 1 unit, then Y increases by B-coeff units.

**Intercept** : Value of predicted Y if both X=0 and Y=0

Intercept is the value or baseline, (organic growth)

**Degrees of freedom** = no of obs - (dimensions of x + dimension of y) = n- (k+1) _\[analogy : 5 hats\]_

**Performance / Observation Window** = Observation window taken when the account was created.

Performance window when the account defaults. Eg if acct defaults in August and perf windows is between feb - july, then its is not considered as default.

A | Feb (Acct created) |

Performance window is rolling window based after the observation window.

Eg perf window for account made in jan would start from feb/march

perf window for account made in feb would start from march/apr

**Linear regression** is a minimization function where the model is built to minimize the sum of squared errors whereas **logistic regression** is a maximization function where the model tries to maximize the parameter values of every variable in such a way that it fits very well on the data
