---
title: Other Algorithms
date: 2020-01-30T00:38:25.000+09:00
description: Regression
weight: 4

---
# Various Algorithms for Regression

As you will see later, there are many algorithms for classification eg decision trees, svm, etc. But what we ignore is that most of these algorithms pack in a regressor along with their classifier as well. Here's some of the classification algorithms which are good fore regression as well.



## Decision Tree Regressor

```
from sklearn.tree import DecisionTreeRegressor
```

> [Read about the classifier algorithm here](/handbook/supervised-learning/classification/decision-trees/) 

## SVM Regressor

```
from sklearn.svm import SVR
```

>  [Read about the classifier algorithm here](/handbook/supervised-learning/classification/support-vector-machine/) 



## Random Forest Regressor 

```
from sklearn.ensemble import RandomForestRegressor
```

 [Read about the classifier algorithm here](/handbook/supervised-learning/classification/random-forest/) 



## Catboost Regressor

```
from catboost import CatBoostRegressor
```

