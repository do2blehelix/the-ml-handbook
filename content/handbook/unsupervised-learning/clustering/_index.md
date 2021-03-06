---
layout: default
has_children: true
title: Clustering
parent: Unsupervised Learning
nav_order: 1
collapsible: true
weight: 1

---
# Clustering

***

Clustering Is a set of data driven partitioning techniques designed to group a collection of objects into clusters.

⚠️ **Data should ALWAYS be continuous and standardized in nature.**

**✴ Clustering is finding borders between groups  
✴ Segmentation is using borders to form groups**

### Applications :

* Market Segmentation
* Sales segmentation : what type of customer wants what
* Credit risk
* Operations : High performing persons and promotions
* Insurance : identifying groups with high average claim cost
* Data reduction : grouping observations to reduce number is obs

 

### How to build clusters :

1. Select distance measure
2. Select clustering algorithm
3. Define the distance between 2 clusters
4. Determine no of clusters
5. Validate the analysis

### Methods

* Linkage method
* Variance method
* Centroid method

### Closeness of two clusters :

The decision of merging two clusters is taken on the basis of closeness of these clusters. There are multiple metrics for deciding:

* Euclidean distance: (a-b)2 = √(Σ(ai-bi))
* Squared Euclidean distance: ((a-b)2)2 = Σ((ai-bi)2)
* Manhattan distance: (a-b)1 = Σ(ai-bi)
* Maximum distance: (a-b)INFINITY = maxi(ai-bi)
* Mahalanobis distance: √((a-b)T S-1 (-b)) {where, s : covariance matrix}

 

 