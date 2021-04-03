---
layout: default
title: Random Forest
parent: Ensemble Learning
grand_parent: Supervised Learning
nav_order: 1
weight: 1
description: Random Forest
date: 2021-04-03 18:30:00 +0000

---
# Random Forest

Random Forest works as a large collection of decorrelated decision trees and is based on bagging (boosted aggregating). 
A random sample is taken from the population with random variables (feature selection)A decision tree is made based on the sample.Multiple samples are taken with replacement (bootstrap sampling)Multiple decision trees are created based on their respective samplesAll the decision trees are used to create a ranking of classesThe final model is based on the most no votes for the class. In case of regression, it takes the average of outputs of different trees.

**Advantages**:Capable of performing both regression and classificationPerforms dimension reduction and handles missing values / outliers effectively.Can handle huge number of variablesShows Importance of variableRF is different from bagging : RF selects a subset of predictors as well. This results in decorrelated trees.
**Disadvantages**:Good at classification but doesn’t provide precise continuous nature predictions for regression Black Box - very little control on what the model does. Only model parameters can be tuned.