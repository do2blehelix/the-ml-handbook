---
layout: default
has_children: true
title: Ensemble Learning
parent: Supervised Learning
nav_order: 3
description: Ensemble Learning
date: 2021-04-03T18:30:00.000+00:00
weight: 3
collapsible: true

---
# Ensemble Learning

Ensemble model combines multiple ‘individual’ (diverse) models together and delivers superior prediction power.

![](https://do2blehelix.github.io/the-ml-handbook/images/supervised/ensemble.jpeg)

### Bagging

Bagging is an approach where you take random samples of data, build learning algorithms and take simple means to find bagging probabilities.

### Boosting

The term ‘Boosting’ refers to a family of algorithms which converts weak learner to strong learners.

### Stacking

First, we use multiple base classifiers to predict the class. Second, a new learner is used to combine their predictions with the aim of reducing the generalization error.

> A good model should maintain a balance between bias-variance. This is known as the trade-off management of bias-variance errors. Ensemble learning is one way to execute this trade off analysis.