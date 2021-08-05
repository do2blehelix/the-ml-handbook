---
title: Regularization
date: 2020-01-30T00:38:25.000+09:00
description: Regularization
weight: 3

---
# Regularization

Regularization is a process of introducing additional information in order to solve an ill-posed problem or to prevent overfitting

## Ridge Regression (L2)

**Ridge regression** is also called **L2 regularization**. It adds a constraint that is a linear function of the squared coefficients.

![](https://miro.medium.com/max/1106/1*iBn8qy31OpJGi3E4oo9tJQ.png)

## Lasso Regression (L1)

**Lasso** is also known as **L1 regularization**. It penalizes the model by the absolute weight coefficients.

![](https://miro.medium.com/max/753/1*L0qFo8VMP1Z6Z9QfqkuQGA.png)

  
**Elastic Net**

**Elastic Net** is the combination of the L1 regularization and L2 regularization. It can both shrink the coefficients as well as eliminate some of the insignificant coefficients.