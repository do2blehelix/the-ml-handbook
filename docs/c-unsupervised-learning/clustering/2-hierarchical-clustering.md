---
layout: default
title: Hierarchical Clustering
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 2

---
# Hierarchical Clustering

It is a set of nested clusters organized as a hierarchical tree. No decision about number of clusters It is not used when data is big due to higher processing time.

### Advantages:

* Produces an additional ability to visualize 
* Potent esp if the data contains real hierarchical relationships (eg evolution) 

### Disadvantages:

* Computationally intensive 
* Sensitive to noise and outliers

### Types :

* Agglomerative : Start from n clusters and get to one cluster  _`Bottom up approach`_
* Divisive : Start from one cluster and get to n clusters  _`Top down approach`_

### Distance Between Clusters (Agglomerative Clustering)

* Single link : Shortest distance between an element in one cluster and an element in another cluster. 
* Complete link : Largest distance between elements in two clusters. Produces compact clusters. 
* Average link : Average distance of elements between 2 clusters. 
* Centroid : Distance between the centroids of 2 clusters 
* Metroid : Distance between centrally located object in both clusters. 
* Ward’s method : Minimize variance between 2 clusters.

The results of hierarchical clustering can be shown using dendrogram.
At the bottom, we start with n data points (observations), each assigned to separate clusters
Two closest clusters are then merged till we have just one cluster at the top
The height in the dendrogram at which two clusters are merged represents the distance between two clusters in the data space.

The best choice of the no. of clusters is the no. of vertical lines in the dendrogram cut by a horizontal line that can transverse the maximum distance vertically without intersecting a cluster.