---
layout: default
parent: Supervised Learning
title: "☑️ Model Evaluation"
nav_order: 4
has_children: false

---
# Model Evaluation / Selection / Fits / Validation

## Train Test Split

* Before running the model, the data is split into `Training` and `Testing` sets.
* The training to test split ratio is generally 70:30 and can vary.
* The model is trained on the `Training` dataset hence the name
* Once the model is fit on the data, we use the `Testing` dataset to check how the model performs.

The model is best served with a k-fold cross validation set where the data is randomly split multiple `k` times and each time the model fit is checked.

***

## Regression Metrics:

* **R Square:** % of variance in `Y` that is explained by `X`. It is defined as the square of correlation between Predicted and Actual values.

**![](https://lh3.googleusercontent.com/q7F8E2RPDOT-odNpAUtV-NLMIEC8cIOUID53ZX_COvkIPu8gvdTy6EG-g9qXPPSp-q1jklJ8BDWBnDd1xlVoyOH_8Szch_MLG-uyub_K69ioQevL9J_QZr4P0qO_PCvtc8lxXezR =153x52)**

R2= SSEIndependent VarSSEIndependent Var + SSEErrors

* **Adjusted R Square:** Similar to R2. It penalizes for adding impurity (insignificant variables) to the model
* **MSE (Mean Squared Error) :**
* **RMSE (Root Mean Square Error)** : It measures standard deviation of the residuals.

Model with the least RMSE is the best model

_= sqrt (Sum of Squared Errors) / no of obs = sqrt (mean ( (Actual - Predicted)2 ))_

![](https://lh3.googleusercontent.com/BMkjNWVQCJSEuhhwB7OcrweuDf43cblmp2yL2uqnKb3PeS0U927ylIohcxuWbq9CcIN_6th0vNw38KW8hpQV1nirzTuvho95ri6DFqBfrdDe1WPEXdidt38UEuuvPBfG9Km0Lcz_ =213x59)

**Mean Square** : Sum of squares / df

* **MAE (Mean Absolute Error) :** sum( |Error| ) / n _Error = Actual - Predicted |Error|=Absolute Error_
* **MAPE (Mean Absolute Percentage Error) :** _{ absolute (average \[ (Actual - Predicted) / Actual \])}_ should not exceed \~ 8% - 10%
* AIC
* BIC

Loss Functions: objective is to minimise these

* MAE : Mean Absolute Error _(mean of the absolute errors)_
* MSE : Mean Squared Error _(mean of the squared errors)_
* RMSE : Root Mean Squared Error _(square root of the mean of squared errors)_

## Classification Metrics :

Accuracy

Precision

Recall

#### Confusion Matrix

| Actual  
|  
|

## ![](https://lh6.googleusercontent.com/V1bR60sTazQxuSSGuoaafLFL2gG53aT3Xe-b37gtsjadm_gIlgoXGGMX5zDGBpVNBOoc9jpDwpbzpVwTwiYe8R5FZZoDc9JZ3BMfgQyB_rpTb3yV0W6Y50-gE7RhqUEUQe2zAbyx =292x219)

#### 

A confusion matrix shows the number of correct and incorrect predictions made by the classification model compared to the actual outcomes (target value) in the data

**Sensitivity :** (True Positive Rate or Recall)

% of actual +ve predicted as +ve = _TP ÷ (TP + FN)_

**Specificity :**

% of actual -ve predicted as-ve = _TN ÷ (FP + TN)_

Positive Predicted Value = _TP ÷ (TP + FP)_

Negative Predicted Value = _TN ÷ (TN + FN)_

Accuracy = (_TP + FP) ÷ (TP + FP + TN + FN)_

Misclassification Rate = _(FP+FN) ÷ (TP + FP + TN + FN) = (1-Accuracy)_

Both sensitivity and specificity should be high for a good model.

**_\[Best Analogy :_** _identifying a single terrorist in a crowd and sniping him vs bombing the place_

_Sniping : high sensitivity ; high specificity || Bombing : high sensitivity ; low specificity\]_

![](https://lh4.googleusercontent.com/FkafGOErm0s0Xoe-A6Jz4sPwzuhkiJG5R78igy7yyF75B3dGphFuDXuCV49deEHcmBsXys33YWMcEXvaS3yt2MdGQI8K87-TMtjSUWLIJrjl0WNJgveMCP_bYtQBwk0kxKpVA1SC =234x58)

* **Precision** _(aka PPV) _: **TP ÷ (TP + FP)**
* **Recall** _(aka Sensitivity)_ : **TP ÷ (TP + FN)**
* **F1 Score : 2x (Precision*Recall) ÷ (Precision+Recall)**

| --- | --- | | TP | FN | | FP | TN |

![](https://lh6.googleusercontent.com/-88NYrtKtm6jDoSaPQOuolCDT-TUMZ9JAJ2In_J5oe8qPpNl5vVH59fCvQrj2YCIqDSbXzi-Us04VI7m9gCNml_ArzF4biKv5fnRjWmutvTY2nxWcgjBdo0ILlDSQIWnmEeNaCaB =209x68)

Medical Model : High Recall Model :: FN should be avoided

Spam Model : High Precision Model :: FP should be avoided

**Beta Score Fβ** _(Range: 0 to ∞)_

(Fβ=0) Precision …… F0.5 ……. F1 …….. F2 ……. Recall (Fβ=∞)

For other values of β, if they are close to 0, we get something close to precision, if they are large numbers, then we get something close to recall, and if β=1, then we get the harmonic mean of precision and recall.

_For the spaceship model, we can't really afford any malfunctioning parts, and it's ok if we overcheck some of the parts that are working well. Therefore, this is a high recall model, so we associate it with beta = 2._

_For the notifications model, since it's free to send them, we won't get harmed too much if we send them to more people than we need to. But we also shouldn't overdo it, since it will annoy the users. We also would like to find as many interested users as we can. Thus, this is a model which should have a decent precision and a decent recall. Beta = 1 should work here._

_For the Promotional Material model, since it costs us to send the material, we really don't want to send it to many people that won't be interested. Thus, this is a high precision model. Thus, beta = 0.5 will work here._

#### ROC (Receiver Operating Characteristics) Curve![](https://lh6.googleusercontent.com/R_1QXnZi0zNM6jWBEZNXpxStbyq-3GVzOCmODRvJSHYNXfPDmEGUgEUsUWFenRl3lELiF4-VZ55Q924V9p0G9dvJzmmw9TbQ8iVJBAxp3IwuhYSbEh8Dr5ZUdrg7q-Wf1QkBvPj3 =302x189)

The ROC chart is plotted with :

Y axis as sensitivity \[True Positive Rate\] and

X axis as (1-specificity) \[False Positive Rate\]

The diagonal line represents a random chance model whereas the line curved towards top left represents how better the model is. The more distant the curve, from the random chance line, the better is the model.

**AUC :** The area under the curve is also used as a quality measure. A random classifier has an area under the curve of 0.5, while AUC for a perfect classifier is equal to 1

c = (%concordant - %discordant + %tied) _÷_ no of pairs

_(random chance)_ **0.5 < c-stat < 1** _(perfect model)_

#### K-S Chart![](https://lh5.googleusercontent.com/tvo-uQPoquKBLLN-vNNiApTart8yLaDVtNskblYlqjZcE1dc2qIAEEWSbPuQ9RFnAVKAJRrdW96ENQe9vdybKCnXneAm0TNYar9bzs4QGApe-wjqK6sD79J63vdlE8eBSdvJXCgZ =297x174)

K-S is a measure of the degree of separation between the positive and negative distributions (events vs non events). It is defined as the maximum difference between cumulative % event and cumulative % non event.

The K-S is 100 if the scores partition the population into two separate groups in which one group contains all the positives and the other all the negatives. If the model selects cases randomly from the population, the K-S would be 0.

KS Statistic is the measure of maximum separability.

_(random chance)_ **0 < K-S < 100** _(perfect model)_

[**EXAMPLE**](https://drive.google.com/open?id=16S4vjIzP1aaxewhxavy-ZgILLE-lL6vujI4BAPWRAUM)

#### Gain and Lift Charts

**Gain** is defined as the cumulative % of target (the ratio of cumulative number of targets (events), to the total number of targets (events))

**Lift** measures how much better one can expect to do with the predictive model comparing without a model. It is the ratio of gain % to the random expectation % at a given decile level. The random expectation at the xth decile is x%.

1. Score (predicted probability) the validation sample using the response model under consideration.
2. Rank the scored file, in descending order by estimated probability
3. Split the ranked file into 10 sections (deciles)

#### Rank Ordering

Same deciles table is created and % of Events is checked to see if there is any discrepancy in downward trend. If the trend is broken then the rank ordering is not maintained.

#### Concordance![](https://lh6.googleusercontent.com/q5z3xrwoK98656UAitBaFqZ1qLWa4G_8GLXt5HfLfHmwykQ33uKfpnVA0QzvcRxiv2rwbFaW7ojeVw1jm5-a-KCo_2ob2HNgX4XySmfGFRBDcI5xlBa8mD8e_bZ-bq-FUKy-zQP8 =151x105)

* Concordant Pair
* Discordant Pair
* Tied Pair

_Percent Concordant = (Number of concordant pairs) / Total number of pairs_

_Percent Discordance = (Number of discordant pairs) / Total number of pairs_

_Percent Tied = (Number of tied pairs) / Total number of pairs_

_Area under curve (c statistics) = Percent Concordant + (0.5 * Percent Tied)_

#### Hosmer and Lemeshow Goodness of Fit

It is carried out to check if the regression explains the variance in data. It sorts the predicted values and groups them into 10 deciles and compares it against the sorted and grouped dependent variable in the original dataset and finds out if any significant difference between observed and expected.

Chi sq test for difference between observed and expected. High p-value indicates good fit.

H0 : The data are consistent with a specified distribution.

HA : The data are **not** consistent with a specified distribution.

#### AIC \[Akaike Information Criterion\]

By adding more parameters, better fit is obtained. However, after a certain point, model tends to overfit.

AIC captures tradeoff between number of parameters added and the incremental amount of error.

Basically, it penalizes models for overfitting of data. Also known as loss criterion.

**Model with lower AIC is better !**

_AIC = - ln L + p L = likelihood p = parameters_

_AIC = N ln (SSerror ÷ N) + 2K N = no of obs K = no of parameters fit+1_

#### BIC \[Bayesian Information Criterion\]

BIC penalizes the number of parameters more than AIC. Emphasizes simplicity of model.

#### Gini (Somers’ D)

Determines the strength and direction of relationships between pairs of variables.

It ranges from -1 (all pairs disagree) to +1 (all pairs agree). Should be gt 0.4

_Somer's D = 2 AUC - 1 = (%concordant - %discordant) / 100_

_= (Concordant pairs - Discordant pairs ) / Total Pairs_

#### Gamma

Similar to Somers’ D but does not penalize for tied pairs.

**Bias - Variance Tradeoff**

Bias : how much on average is my predicted values different from actual values. High bias is underfitting.

Variance : how different will predictions be, at the same point, if different samples are taken from the same population. High variance causes overfitting.

![](https://lh5.googleusercontent.com/QNFSL6we1fCDjTMHUUqz-WnKg_JuldfEulTu2qvDX7ZoDgoSxFAVhejDThCMLTRzfDqRs7Xll9ECL6NU7x6joEWnY0KXJsEePFabL5cH9pq0k6ya3Lxfyt9iguICnf7PfdXxlX2F =286x170)

high bias = high (pred - act) = high error = underfit model

high variance = high sensitivity in changes in data = overfit model

**When a model has high bias, this means that it doesn't do a good job of bending to the data**

**When a model has high variance, this means that it changes drastically to meet the needs of every point in our dataset**

High Bias, Low Variance models tend to underfit data, as they are not flexible. Linear models fall into this category of models.

High Variance, Low Bias models tend to overfit data, as they are too flexible. Decision trees fall into this category of models.

![](https://lh4.googleusercontent.com/ga9WJ0VSA54deurET54OU6jSsyfQcOFCfABQlXpqVonjll7dvCCz_17NvBrfxrAYS1uXR4XYxDkWoeDkxsYgvirMNjbATe8b1Yjvm2YfhCZ-ZzmSQFAKLSEvv0j6KSjD7XfjqQN- =492x246)

Model Complexity Graph : Plots the training and testing error and helps find the optimal point between underfitting and overfitting.

* 

### Validation :

#### K-fold cross Validation

* Sample is partitioned into k equal sized subsamples.
* A single subsample is used as the validation dataset for testing the model.
* Remaining k-1 subsamples are used as training data.
* The cross validation process is repeated k times.

**Advantages**

All observations are used for both training and validation.

Each of the k subsamples used exactly once as the validation data.

#### Learning Curves

![](https://lh5.googleusercontent.com/zHfafLEPe9jlrCSeRDQFivuKWDhpNAMsltF8Ulh0-bRd0ANAXuWsrsSn5lyUJI30q2l7Q_sx3-1Qae7Xgr3MmSf53yi7tAPxnCW4oRmrXvxWRgG_F3yooM3f19eYF4DzT1u0SUqZ =427x181)

#### Grid Search

Technique used to list down all the possibilities of the hyperparameters and pick the best one.

**MODEL MONITORING**

Population Stability Index (PSI)

1. Sort scoring variable on descending order in scoring sample
2. Split the data into 10 or 20 groups (deciling)
3. Calculate % of records in each group based on scoring sample
4. Calculate % of records in each group based on training sample
5. Calculate difference between Step 3 and Step 4
6. Take Natural Log of (Step3 / Step4)
7. Multiply Step5 and Step6

continue model < 0.1 < slight change < 0.2 < significant change