---
title: Hypothesis Testing
date: 2020-01-30T00:38:25+09:00
description: Hypothesis Testing
weight: 5


---
# Hypothesis Testing
It the the action of declaring a hypothesis (a fundamental logical component) and proving its occurrence of proving its non-existence.

## Types of Hypothesis

### Null Hypothesis
>**H<sub>0</sub> : μ1 = μ2x <br>**
The means of the two groups (μ1 & μ2) belong to the same population. _(p > 0.05)_


### Alternative Hypothesis
>**H<sub>A</sub> : μ1 ≠ μ2**  
The means of the two groups (μ1 & μ2) belong to different populations. In case of multiple groups, the mean of all groups shouldn’t be the same. At least one group should be different. _(p < 0.05)_

***

### Significance level : α

The significance level, also denoted as alpha or α, is the probability of rejecting the null hypothesis when it is true. Typically _0.05 (5%)_

### Confidence level : (1 - α)

---

&nbsp;
&nbsp;


## Errors


**Type I** : Rejecting the null hypothesis even if it's true `False Positive`

**Type II** : Accepting the null hypothesis even when it's false `False Negative`

Probability (type I error) = **α** | Probability (type II error) = **β**

---

&nbsp;

**Analogy**

Person on trial :   
`Null = He is innocent` &nbsp;&nbsp; `Alternate = He is guilty`  
**Type I** : reject the null when true : he is innocent but rejected : innocent person in jail ⛔ _avoid_  
**Type II** : accept the null when false : he is guilty but declared innocent : guilty person free

Person with cancer :   
`Null = Doesn't have cancer` &nbsp;&nbsp; `Alternate = Has cancer`   
**Type I** : reject the null when true : doesn’t have but detected : person lives   
**Type II** : accept the null when false : has but not detected : person dies ⛔ _avoid_

![](https://lh6.googleusercontent.com/7AEIDqZ7cCJpgMuonbteAzU9k6PAik6sNpHZ2YoAnTqzkwzi6lbA_jIoIsuIRm_qP6cv1zKOudp8K-Durmu4LNCYiGjuXVHTgY9Oty6gxyBDViZX1GIXd1QRx8dxFxno2_-rqI0y)

&nbsp;

**Misclassification Errors** (Confusion Matrix)

| Actuals ⏬ | Predicted ⏩ |  |
| --- | --- | --- |
|  | Pred ✔️ | Pred ❌ |
| Act ❌ | FP | TN |
| Act ✔️ | TP | FN |
