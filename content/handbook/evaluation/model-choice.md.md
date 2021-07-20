---
layout: default
parent: Supervised Learning
title: Model Choice
nav_order: 4
has_children: false
description: Choosing the right model
date: 2021-04-03T18:30:00.000+00:00
weight: 5
collapsible: false

---
# Choice of Model Metrics

## Precision vs Recall Model

Precision

## Bias vs Variance Model

**Bias - Variance Tradeoff**

Bias : how much on average is my predicted values different from actual values. High bias is underfitting.

Variance : how different will predictions be, at the same point, if different samples are taken from the same population. High variance causes overfitting.

![bias-variance.png](https://github.com/do2blehelix/the-ml-handbook/blob/master/static/images/evaluation/bias-variance.png?raw=true)

high bias = high (pred - act) = high error = underfit model

high variance = high sensitivity in changes in data = overfit model

**When a model has high bias, this means that it doesn't do a good job of bending to the data**

**When a model has high variance, this means that it changes drastically to meet the needs of every point in our dataset**

High Bias, Low Variance models tend to underfit data, as they are not flexible. Linear models fall into this category of models.

High Variance, Low Bias models tend to overfit data, as they are too flexible. Decision trees fall into this category of models.

![overfitting-training.png](https://github.com/do2blehelix/the-ml-handbook/blob/master/static/images/evaluation/overfitting-training.png?raw=true)

Model Complexity Graph : Plots the training and testing error and helps find the optimal point between underfitting and overfitting.