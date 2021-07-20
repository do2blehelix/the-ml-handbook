---
layout: default
parent: Supervised Learning
title: "☑️ Regression Metrics"
nav_order: 4
has_children: false
description: Regression Evaluation
date: 2021-04-03T18:30:00.000+00:00
weight: 1

---
## Regression Metrics:

* **R Square:** % of variance in `Y` that is explained by `X`. It is defined as the square of correlation between Predicted and Actual values.  
  `R2= SSEIndependent VarSSEIndependent Var + SSEErrors`
* **Adjusted R Square:** Similar to R2. It penalizes for adding impurity (insignificant variables) to the model
* **MSE (Mean Squared Error) :** Sum of squares / df
* **RMSE (Root Mean Square Error)** : It measures standard deviation of the residuals.

  `Model with the least RMSE is the best model`  
  `RMSE =`  _`sqrt (Sum of Squared Errors) / no of obs = sqrt (mean ( (Actual - Predicted)2 ))`_
* **MAE (Mean Absolute Error) :** `sum( |Error| ) / n`_`Error = Actual - Predicted |Error|=Absolute Error`_
* **MAPE (Mean Absolute Percentage Error) :** _`{ absolute (average [ (Actual - Predicted) / Actual ])}`_ should not exceed \~ 8% - 10%
* AIC
* BIC

![r2.png](https://github.com/do2blehelix/the-ml-handbook/blob/master/static/images/evaluation/r2.png?raw=true)![rmse.png](https://github.com/do2blehelix/the-ml-handbook/blob/master/static/images/evaluation/rmse.png?raw=true)

**Loss Functions:** objective is to minimize these

* MAE : Mean Absolute Error _(mean of the absolute errors)_
* MSE : Mean Squared Error _(mean of the squared errors)_
* RMSE : Root Mean Squared Error _(square root of the mean of squared errors)_