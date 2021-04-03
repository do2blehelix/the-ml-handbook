---
layout: default
title: Naive Bayes
parent: Classification
grand_parent: Supervised Learning
nav_order: 3
---



# Naïve Bayes

It is a classification technique based on Bayes’ theorem with an assumption of independence between predictors. In simple terms, a Naive Bayes classifier assumes that the presence of a particular feature in a class is unrelated to the presence of any other feature.![img](https://lh6.googleusercontent.com/0LRN5o2He3qiZDOFP6BAZLoeLU-R9-HXyKDhQrARPoLeCaL-y7XX74EydH3PGUB5khvv-7aseVOtqUTYTdQsoKxXiIfano8y5cWEDnDvhr7J8LR_biiwWq6BvFoaJZd1bU-dqo1v)

- *P(c|x) is the posterior probability of class (target) given predictor (attribute).* 
- *P(c) is the prior probability of class.* 
- *P(x|c) is the likelihood which is the probability of predictor given class.* 
- *P(x) is the prior probability of predictor.*



### Calculation

- Convert the data set to frequency table

- Create Likelihood table by finding the probabilities

- Now, use Naive Bayesian equation to calculate the posterior probability for each class. The class with the highest posterior probability is the outcome of prediction.

  

Naive Bayes predicts the probability of different class based on various attributes. This algorithm is mostly used in text classification and with problems having multiple classes.

|                              |                            |      |
| ---------------------------- | -------------------------- | ---- |
| Known P(A)                   | *Probability of A*         |      |
| Known P(R\|A)                | *Probability of R given A* |      |
| Bayes theorem infers P(A\|R) | *Probability of A given R* |      |



> This is the 'Naive' bit of the theorem where it considers each feature to be independent of each other which may not always be the case and hence that can affect the final judgement.