---
layout: default
parent: Supervised Learning
title: Model Validation
nav_order: 4
has_children: false
description: Model Evaluation / Selection / Fits / Validation
date: 2021-04-03T18:30:00.000+00:00
weight: 2

---
# Model Evaluation / Selection / Fits / Validation

## Train Test Split

* Before running the model, the data is split into `Training` and `Testing` sets.
* The training to test split ratio is generally 70:30 and can vary.
* The model is trained on the `Training` dataset hence the name
* Once the model is fit on the data, we use the `Testing` dataset to check how the model performs.

The model is best served with a k-fold cross validation set where the data is randomly split multiple `k` times and each time the model fit is checked.

***

## Validation :

### K-fold cross Validation

* Sample is partitioned into k equal sized subsamples.
* A single subsample is used as the validation dataset for testing the model.
* Remaining k-1 subsamples are used as training data.
* The cross validation process is repeated k times.

#### Advantages

All observations are used for both training and validation.

Each of the k subsamples used exactly once as the validation data.

#### Learning Curves

![](https://lh5.googleusercontent.com/zHfafLEPe9jlrCSeRDQFivuKWDhpNAMsltF8Ulh0-bRd0ANAXuWsrsSn5lyUJI30q2l7Q_sx3-1Qae7Xgr3MmSf53yi7tAPxnCW4oRmrXvxWRgG_F3yooM3f19eYF4DzT1u0SUqZ =427x181)

## Grid Search

Technique used to list down all the possibilities of the hyperparameters and pick the best one.

## Model Monitoring

Population Stability Index (PSI)

1. Sort scoring variable on descending order in scoring sample
2. Split the data into 10 or 20 groups (deciling)
3. Calculate % of records in each group based on scoring sample
4. Calculate % of records in each group based on training sample
5. Calculate difference between Step 3 and Step 4
6. Take Natural Log of (Step3 / Step4)
7. Multiply Step5 and Step6

continue model < 0.1 < slight change < 0.2 < significant change