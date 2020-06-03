---
layout: default
parent: Unsupervised Learning
title: Clustering
nav_order: 1

---
# Clustering

***

Is a set of data driven partitioning techniques designed to group a collection of objects into clusters.

**⭐ Clustering is finding borders between groups**

**⭐ Segmentation is using borders to form groups**

&nbsp;

**Methods**

* Linkage method
* Variance method
* Centroid method

&nbsp;

**Applications :**

* Market Segmentation
* Sales segmentation : what type of customer wants what
* Credit risk
* Operations : High performing persons and promotions
* Insurance : identifying groups with high average claim cost
* Data reduction : grouping observations to reduce number is obs

&nbsp;

The decision of merging two clusters is taken on the basis of closeness of these clusters. There are multiple metrics for deciding the   
**Closeness of two clusters :**

* Euclidean distance: ||a-b||2 = √(Σ(ai-bi))
* Squared Euclidean distance: ||a-b||22 = Σ((ai-bi)2)
* Manhattan distance: ||a-b||1 = Σ|ai-bi|
* Maximum distance:||a-b||INFINITY = maxi|ai-bi|
* Mahalanobis distance: √((a-b)T S-1 (-b)) {where, s : covariance matrix}

&nbsp;

**How to build clusters :**

Select distance measure > Select clustering algorithm > Define the distance between 2 clusters >

Determine no of clusters > Validate the analysis

&nbsp;

**Data should ALWAYS be continuous and standardized in nature.**