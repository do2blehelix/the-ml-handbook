---
layout: default
title: Decision Trees
parent: Classification
grand_parent: Supervised Learning
nav_order: 2
description: Decision Trees
date: 2021-04-03T18:30:00.000+00:00
weight: 2

---
# Decision Trees

It's a type of supervised learning algorithm mostly used for classification problems. Works for **both categorical and continuous** variables.

The population is split into two or more homogeneous sets based on the splitting criterion.

> _Analogy : They ask a bunch of questions to arrive at a particular answer. (20 Questions)_

**Types :**

* Categorical Variable Decision Tree : Categorical Target Variable
* Continuous Variable Decision Tree : Continuous Target Variable

### Advantages

* Glass-box model. Patterns easy to understand and see.
* Useful in Data exploration : fastest way to find most significant variables and relation between variables. new variables can also be created with better prediction power.
* Less data cleaning required : not influenced by missing values and outliers to a fair degree
* Data type is not a constraint
* Non Parametric Method : no assumptions

### Disadvantages

* Over fitting : If no limit is set for a decision tree, it will give 100% accuracy on training set
* Not fit for continuous variables : tends to lose information when bucketed into categories.

### Implementation

```python
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier()    # Instantiate
model.fit(X_train, y_train)  		# Fit model
```

### Terminology

* Root Node : It represents the entire population / sample
* Parent and Child Node: A node, which is divided into sub-nodes is called parent node whereas sub-nodes are the child of parent node.
* Leaf / Terminal Node : Nodes that do not spit any further.
* Branch / Sub-tree : Sub section of the entire tree.
* Splitting : Process of dividing a node into two or more sub-nodes.
* Pruning : The process of removing sub-sections of a tree.
* Grafting : The process of adding a whole section to the tree.

### Hyperparameter (Tuning)

* Maximum Depth : The maximum number of levels in the tree
* Minimum number of samples to split : minimum required samples in node in order for it to further split
* Minimum number of samples per leaf : If it's an integer, it's the minimum number of samples required in a leaf. If it's a float, it's the minimum percentage of samples required in a leaf

**Constraints :**

Overfitting is one of the key challenges faced while modeling decision trees. If there is no limit set of a decision tree, it will give you 100% accuracy on the training set because in the worst case it will end up making 1 leaf for each observation. Thus, preventing overfitting is pivotal while modeling a decision tree and it can be done in 2 ways:

* Setting constraints  `pre pruning`
  * Minimum samples required for a node split
  * Minimum samples at a terminal node (leaf)
  * Maximum depth of tree (vertical depth)
  * Maximum number of terminal nodes
  * Maximum features to consider for split
* Tree Pruning `post pruning`
  * We first make the decision tree to a large depth.
  * Then we start at the bottom and start removing leaves which are giving us negative returns when compared from the top.
  * Suppose a split is giving us a gain of say -10 (loss of 10) and then the next split on that gives us a gain of 20. A simple decision tree will stop at step 1 but in pruning, we will see that the overall gain is +10 and keep both leaves.

### Validation

* SSE
* Classification/confusion matrix

### Metrics

#### **Gini Index** _\[Categorical\]_

The gini measure gives the probability that 2 items chosen from the same population at random are in the same class. For a pure population this probability is 1.

* It works with categorical target variable “Success” or “Failure”.
* It performs only Binary splits
* Higher the value of Gini, higher the homogeneity.
* CART (Classification and Regression Tree) uses Gini method to create binary splits.

Gini Score :

S**1** : \[ (a ÷ t**1** )2 + (b ÷ t**1** )2 \] = g**1**

S**2** : \[ (a ÷ t**2** )2 + (b ÷ t**2** )2 \] = g**2**

_T = t**1** + t**2** = total 1 + total 2_

Final gini score = \[ g**1** **x** (t**1**/T) \] + \[ g**2** **x** (t**2**/T) \]

#### **Chi-Square** _\[Categorical\]_

It is used to find the statistical significance of the differences between sub nodes and parent node. Measured by the sum of squares of standardized differences between observed and expected frequencies of target variable.

* It works with categorical target variable “Success” or “Failure”.
* It can perform two or more splits.
* Higher the value of Chi-Square, higher the statistical significance of differences between sub-node and Parent node or better the split.
* It generates tree called CHAID (Chi-square Automatic Interaction Detector)![](https://lh3.googleusercontent.com/9Q1JXlB5IUqr33_g3XflcYXaTtyddWv9aV3xMGqEFZ_9-XgULoeyHmdiPchP5DzBrkeuRRzAZpz9Qf8zLoJXweU-rqKEGnguFnFWlb2rUwNF13Ec15JpUQq7BKH56DUqWG-HrG2o =217x79)

Chi-Square of each node is calculated using formula,

Chi-square = ((Actual – Expected)^2 / Expected)^1/2

#### **Information Gain** _\[Categorical\]_

Information theory is a measure to define this degree of disorganization in a system known as Entropy. If the sample is completely homogeneous, then the entropy is zero and if the sample is an equally divided (50% – 50%), it has entropy of one. Based on the concept that impure nodes require more information to describe it and vice versa.

![](https://lh4.googleusercontent.com/rcMfiGKMgvSZzjPnQX33elyNQdYUwaxpTvsWdwPx8iCWLLLtNiSDjd6lxwV8IYPcjnklyeW2cKr-g7l0Ljv-4yTdZv3bSiVnuZc23Usjh9nqk4RwmBTU9sEwCQ488T4rQs5lPYYo =218x30)

_Here p and q is the probability of success and failure respectively in that node._ The lesser the entropy, the better it is.

Information Gain = 1 - Entropy

![](https://lh4.googleusercontent.com/zybRY0XxMY_eYoZsmIEtr-uvOt7958kk9xRpU-kQGYAsriJ6wWiGbNlfzjFyJ3ORsw0aB_fLtH2VnS331upispJ9wq6XkIgZP5RbZ_q1i9XBx1Ggm1MkneH6sjj5ct4aP0gF3TAK =131x57)![](https://lh3.googleusercontent.com/wBBoA_r9sduFgt_mtm7xSfnhT0i2G1_RyHZjVl-fvgjj2dMBbd_yS7SG5wuECHk4wBz87nXkesKrLI-TiivQUCum-0C0sIg2II9moYb71Aq5TI06O8L6g5HXi36e88GeKKaKiFV5 =133x65)

![](https://lh3.googleusercontent.com/R8d8virMuQKr9epf4yd1WkzWkIL8yu3h4K9HJhzrt9YjV43NK988Id0Qwvtsyi9VniiqlqkrgdnJS0hWOYcX2IDkv7Wdcmyg0Bnlwj4yVZRucRGIWH34D-8d_blNCegSKY4Ejud9 =442x50)

![](https://lh6.googleusercontent.com/u4RjBDBarEnYDWaF25iPUsi3J_sTFJjT9YtezaDcLT0Vi-G9OVO0v9b-sia1rKJd93mkeTseiaedreDQQnKLRu1dToY4k-PWCTUUMpU5NGD_rxwNE52fABjDdJkm_-3KFld8_N65 =318x31)

![](https://lh4.googleusercontent.com/jRsSIsIBpkX8XQZfggQ0GbXnfHScx2rSyRUx70T_qQPtyNAPWOQIQ_jNLTLUIXN-Uq0f1I-7937R45RBum224v8S2RnhTh1eeiO3sGfPcq_-mUu5ubmVRHOjREXZzoJmKLXg_sm0 =720x60)

#### **Reduction in Variance** _\[Continuous\]_

![](https://lh6.googleusercontent.com/Ud0tg7MutTJjtjmZRhtsHy52aF6z78mNlhwvMUL95-dAFZEexKbnbLKXoXatkCtr8oH44wHTve7vPo9t102DdlV9zsM5ucWyWl8KuYA9XaLsB1dhKa_tdDwRgPe_cdFVNLy6FzZb =176x53)

Reduction in variance is an algorithm used for continuous target variables (regression problems). This algorithm uses the standard formula of variance to choose the best split. The split with lower variance is selected as the criteria to split the population

_X-bar is mean of the values, X is actual and n is number of values._

### Algorithms

#### CART : Classification And Regression Trees

Decides on split based on the amount of homogeneity within class that is achieved by the split.

_Classification y is categorical_

_Regression y is continuous_

* CART first grows the full tree using training set and then prunes it back using holdout set.
* **Allows only binary splits.**

Gini algorithm

#### ID3 > C4.5 > C5.0 :

Splitting criterion is the normalized information gain (difference in information entropy). The attribute with the highest normalized information gain is chosen to make the decision. It is the successor of ID3.

* C4.5/5.0 first grows the full tree using training set and then uses single dataset to arrive at final tree.
* **Allows multiple split.**

#### CHAID : Chi-square Automatic Interaction Detector

Tests a hypothesis regarding dependence between the split variable and the categorical response (using chi-square test for independence)

* Similar to regression analysis, it selects best predictors that account for the most explained variable
* Chaid goes one step further and identifies the important elements : those variables that most differentiate target variable.
* Chaid begins by finding variables that have significant association with target variable
* It assesses the category groupings or interval breaks to pick the most significant combination of variables
* The variable having the strongest association with the target variable becomes the first branch in a tree with lead for each category that is significantly different relative to target variable.
* The process is repeated to find the predictor variable on each leaf most significantly related to the target variable, until no significant predictors remain.
* Chaid uses statistical stopping rule that discontinues tree growth. It uses training dataset
* **Allows multiple split.**