---
layout: default
title: Gradient Boosting
parent: Ensemble Learning
grand_parent: Supervised Learning
nav_order: 2
weight: 2
description: Gradient Boosting
date: 2021-04-03T18:30:00.000+00:00

---
# Boosting Algorithms

1. The base learner takes all the distributions and assign equal weight or attention to each observation.
2. If there is any prediction error caused by first base learning algorithm, then we pay higher attention to observations having prediction error. Then, we apply the next base learning algorithm.
3. Iterate Step 2 till the limit of base learning algorithm is reached or higher accuracy is achieved. weight = ln ( accuracy / (1-accuracy) ) = ln (correctly classified / incorrectly classified)

> The fundamental difference between Bagging and Random Forest is that in Random forests, only a subset of features are selected at random out of the total and the best split feature from the subset is used to split each node in a tree, unlike in bagging where all features are considered for splitting a node.

## Gradient Boosting (GBM) 

    from sklearn.ensemble import GradientBoostingClassifier

## AdaBoost

    from sklearn.ensemble import AdaBoostClassifier

## XG Boost

    from xgboost import XGBClassifier

## Catboost