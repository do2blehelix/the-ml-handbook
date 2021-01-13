---
layout: default
title: Knowledge Repository
nav_order: "6"

---
# The Important Stuff Everyone Misses!

* **Multivariate Analysis** is nothing but regression
* Logistic regression IS a binomial regression (with logit link), a special case of the Generalized Linear Model. It doesn't classify anything _unless a threshold for the probability is set_. Classification is just its application.
* Stepwise regression is by no means a regression. It's a (flawed) method of variable selection.
* OLS is a method of estimation (among others: GLS, TLS, (RE)ML, PQL, etc.), NOT a regression.
  Ridge, LASSO - it's a method of regularization, NOT a regression.
* There are tens of models for the regression analysis. You mention mainly linear and logistic - it's just the GLM! Learn the others too (link in a comment). STOP with the "17 types of regression every DS should know".BTW, there're 270+ statistical tests. Not just t, chi2 & Wilcoxon

6 Types of Data Analysis you will do as a Data Scientist  
  
1\. Descriptive - Present a report of what has happened already. Usually involves using basic measures of statistics to represent findings.  
  
2\. Exploratory - Open-ended exploration to check for patterns, trends or relationships.  
  
3\. Inferential - Looking at a sample dataset available to you and making inferences from it on the population. In other words, running experiments (if possible), getting data and drawing inferences about the population.  
  
4\. Predictive - Predicting labels or things that may occur in the future based on signals from the past.  
  
5\. Causal - Identifying if a change in one factor leads to a change in other factors or the entire population and to what extent.  
  
6\. Mechanistic - Finding the underlying mechanism of the observed patterns, trends or relationships. Trying to answer the how of the occurrence.