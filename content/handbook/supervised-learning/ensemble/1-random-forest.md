---
layout: default
title: Random Forest
parent: Ensemble Learning
grand_parent: Supervised Learning
nav_order: 1
weight: 1
description: Random Forest
date: 2021-04-03T18:30:00.000+00:00

---
# Bagging Algorithms

    from sklearn.ensemble import BaggingClassifier

## Random Forest

    from sklearn.ensemble import RandomForestClassifier

Random Forest works as a large collection of decorrelated decision trees and is based on bagging (boosted aggregating).

1. A random sample is taken from the population with random variables (feature selection)
2. A decision tree is made based on the sample.
3. Multiple samples are taken with replacement (bootstrap sampling)
4. Multiple decision trees are created based on their respective samples.
5. All the decision trees are used to create a ranking of classes.
6. The final model is based on the most number votes for the class. _In case of regression, it takes the average of outputs of different trees._

### Advantages

* Capable of performing both regression and classification
* Performs dimension reduction and handles missing values / outliers effectively.
* Can handle huge number of variables
* Shows Importance of variable
* RF is different from bagging : RF selects a subset of predictors as well. This results in decorrelated trees.

### Disadvantages

* Good at classification but doesn’t provide precise continuous nature predictions for regression
* Black Box - very little control on what the model does. Only model parameters can be tuned.