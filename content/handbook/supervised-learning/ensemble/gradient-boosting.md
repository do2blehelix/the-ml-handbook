---
layout: default
title: Boosting
parent: Ensemble Learning
grand_parent: Supervised Learning
nav_order: 2
weight: 2
description: Gradient Boosting
date: 2021-04-03T18:30:00.000+00:00

---
# Boosting

The term ‘Boosting’ refers to a family of algorithms which converts weak learner to strong learners.

1. It starts by assigning equal weights to each observation.
2. Base learning algorithm is applied.
3. If there is a prediction error, then the misclassified observations are assigned a higher weightage.
4. Next base learning algorithm is applied.
5. The iteration continues until the limit of learning algorithm is reached or higher accuracy is achieved.

Finally, it combines the outputs from weak learner and creates a strong learner which eventually improves the prediction power of the model. Boosting pays higher focus on examples which are mis-classiﬁed or have higher errors by preceding weak rules.

> It has shown better predictive accuracy than bagging, but it also tends to overfit the training data as well.

![](https://do2blehelix.github.io/the-ml-handbook/images/ensemble.jpeg)

1. The base learner takes all the distributions and assign equal weight or attention to each observation.
2. If there is any prediction error caused by first base learning algorithm, then we pay higher attention to observations having prediction error. Then, we apply the next base learning algorithm.
3. Iterate Step 2 till the limit of base learning algorithm is reached or higher accuracy is achieved. weight = ln ( accuracy / (1-accuracy) ) = ln (correctly classified / incorrectly classified)
4. 

## Gradient Boosting (GBM)

    from sklearn.ensemble import GradientBoostingClassifier

## AdaBoost

    from sklearn.ensemble import AdaBoostClassifier

## XG Boost

    from xgboost import XGBClassifier

XGBoost stands for Xtreme Gradient Boosting. It is a decision-tree-based ensemble Machine Learning algorithm that uses a gradient boosting framework. Can be used to solve regression, classification, ranking, and user-defined prediction problems. XGBoost and Gradient Boosting Machines (GBMs) are both ensemble tree methods that apply the principle of boosting weak learners (CARTs generally) using the gradient descent architecture. However, XGBoost improves upon the base GBM framework through systems optimization and algorithmic enhancements.

## Catboost