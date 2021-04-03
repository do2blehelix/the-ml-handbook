---
layout: default
parent: Unsupervised Learning
title: KNN
nav_order: 2
has_children: false

---
# KNN (K- Nearest Neighbors)

It is a simple algorithm which classifies cases based on its votes by its nearest neighbors whose class is already known. The “K” is KNN algorithm is the number of nearest neighbors we wish to take vote from. The class to be chosen depends on a distance function.

_Categorical : Euclidean, Manhattan, Minkowski  
Continuous : Hamming_

### Advantages:

* Attributes with multiple missing values can be easily treated
* Can predict both qualitative & quantitative (by taking average) attributes
* Easy interpretation. Low calculation time.