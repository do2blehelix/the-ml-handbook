---
layout: default
title: Hierarchical Clustering
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 2
description: Introduction and Implementation of Unsupervised learning algorithm Hierarchical
  Clustering
date: 2021-04-05T18:30:00.000+00:00
weight: 2

---
# Hierarchical Clustering

It is a set of nested clusters organized as a hierarchical tree. No decision about number of clusters It is not used when data is big due to higher processing time.

### Types

* **Agglomerative** : Start from n clusters and get to one cluster  `Bottom up approach`
* **Divisive** : Start from one cluster and get to n clusters  `Top down approach`

### Advantages

* Produces an additional ability to visualize
* Potent, especially if the data contains real hierarchical relationships (eg evolution)

### Disadvantages

* Computationally intensive
* Sensitive to noise and outliers

### Distance Between Clusters (Agglomerative Clustering)

* Single link : Shortest distance between an element in one cluster and an element in another cluster.
* Complete link : Largest distance between elements in two clusters. Produces compact clusters.
* Average link : Average distance of elements between 2 clusters.
* Centroid : Distance between the centroids of 2 clusters
* Metroid : Distance between centrally located object in both clusters.
* Ward’s method : Minimize variance between 2 clusters.

### Visualization

![](https://do2blehelix.github.io/the-ml-handbook/images/unsupervised/hierarchical_dendogram.png)The results of hierarchical clustering can be shown using **dendrogram**.

1. At the bottom, we start with n data points (observations), each assigned to separate clusters.
2. Two closest clusters are then merged till we have just one cluster at the top
3. The height in the dendrogram at which two clusters are merged represents the distance between two clusters in the data space.

_The best choice of the no. of clusters is the no. of vertical lines in the dendrogram cut by a horizontal line that can transverse the maximum distance vertically without intersecting a cluster._