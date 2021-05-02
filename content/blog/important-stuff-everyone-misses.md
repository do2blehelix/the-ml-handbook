---
title: "The Important Stuff Everyone Misses"
description: "The Important Stuff Everyone Misses"
date: 2020-01-28T00:10:48+09:00
weight: 1
image: https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8ZGF0YXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60
enableToc: false
tocLevels: []
tags: ["Data Analysis", "Algorithms"]
---

# Easy to Overlook these



- **Multivariate Analysis** is nothing but regression



- Logistic regression IS a binomial regression (with logit link), a special case of the Generalized Linear Model. It doesn't classify anything **unless a threshold for the probability is set**. Classification is just its application.

- Stepwise regression is by no means a regression. It's a (flawed) method of variable selection.

- OLS is a method of estimation (among others: GLS, TLS, (RE)ML, PQL, etc.), NOT a regression.

 Ridge, LASSO - it's a method of regularization, NOT a regression.

- There are tens of models for the regression analysis. You mention mainly linear and logistic - it's just the GLM! Learn the others too (link in a comment). STOP with the "17 types of regression every DS should know".BTW, there're 270+ statistical tests. Not just t, chi2 & Wilcoxon