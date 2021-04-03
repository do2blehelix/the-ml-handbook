---
layout: default
has_children: true
title: Ensemble Learning
parent: Supervised Learning
nav_order: 3

---

﻿# Ensemble Learning

Ensemble model combines multiple ‘individual’ (diverse) models together and delivers superior prediction power. A good model should maintain a balance between bias-variance. This is known as the trade-off management of bias-variance errors. Ensemble learning is one way to execute this trade off analysis.

**Bagging :**Bagging is an approach where you take random samples of data, build learning algorithms and take simple means to find bagging probabilities.Objective is to average noisy and unbiased models to create a model with low variance
Create Multiple DataSets:Sampling is done with replacement on the original data and new datasets are formed.The new data sets can have a fraction of the columns as well as rows, which are generally hyper-parameters in a bagging modelTaking row and column fractions less than 1 helps in making robust models, less prone to overfittingBuild Multiple Classifiers:Classifiers are built on each data set.Generally the same classifier is modeled on each data set and predictions are made.Combine Classifiers:The predictions of all the classifiers are combined using a mean, median or mode value depending on the problem at hand.The combined values are generally more robust than a single model.

**Boosting :**The term ‘Boosting’ refers to a family of algorithms which converts weak learner to strong learners.It starts by assigning equal weights to each observation.Base learning algorithm is applied. If there is a prediction error, then the misclassified observations are assigned a higher weightage.Next base learning algorithm is applied.The iteration continues until the limit of learning algorithm is reached or higher accuracy is achieved.Finally, it combines the outputs from weak learner and creates a strong learner which eventually improves the prediction power of the model. Boosting pays higher focus on examples which are mis-classiﬁed or have higher errors by preceding weak rules.![img](https://lh5.googleusercontent.com/BY-CmyGn_ZsjMfktN6EhmW41CUgZQmIXlNE7jmkSwMFsq5ibc1BHgP1BjFIbJyCDzvM3YtAjCHxZhazjNLpGg5prA64waM1Brxy3JDFID3r0DTXAsHzy22ppZwRlyWI9KEfpN_of)It has shown better predictive accuracy than bagging, but it also tends to overfit the training data as well. 

**Stacking** works in two phases. First, we use multiple base classifiers to predict the class. Second, a new learner is used to combine their predictions with the aim of reducing the generalization error.