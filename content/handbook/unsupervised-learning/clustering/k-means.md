---
layout: default
title: K-Means
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 1
weight: 1
date: 2021-04-05T18:30:00.000+00:00
description: Introduction to K-means Unsupervised Algorithm and application

---
# K means (Non Hierarchical)

    from sklearn.cluster import KMeans

It is based on division of objects into non overlapping subsets. Main objective is to form clusters that are homogeneous in nature and heterogeneous to each other.  
❕ **Only for continuous variables.**

### Advantages

* Faster, more reliable, works with large data.
* Computationally lighter than other methods

### Disadvantages

* Can only identify clusters circular / spherical in nature. _(check crescent dataset)_
* Distance based

### Process

1. Identify **value of _‘k’_**
2. Assign **random k observations** as seeds
3. Assign **each record to one of the k seeds** based on proximity
4. **Form clusters**
5. **Calculate centroids** of clusters
6. Assign **centroids as new seed**
7. Form **new clusters**
8. **Recalculate** clusters
9. Continue process until **stable clusters** are formed (boundary ceases to change)

#### Elbow Criterion (Scree Plot):

![](https://do2blehelix.github.io/the-ml-handbook/images/unsupervised/kmeans_screeplot.png)

K means clustering doesn't provide an estimate of the number of clusters required. Hence elbow criterion is used to determine optimal number of clusters.

The method states that you should choose a number of clusters so that adding another cluster does not add any sufficient information. It is plotted by **ratio of within cluster variance to between cluster variance** against number of clusters. The objective is to minimize the within and maximize the between distances.

### Validation:

* Silhouette Index
* Davies Bouldin Score
* Calinski Harabasz Score
* Pseudo F

### Parameter Tuning

    km = Kmeans(n_clusters=2, max_iter=100)
    km.fit(X_std)