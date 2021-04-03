---
layout: default
title: DBSCAN
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 3

---
# Density Based Spatial Clustering of Applications with Noise _(DBSCAN)_ 

 DBSCAN clusters densely packed points and labels the other points as noise. 

### Advantages:

* No specification of no of clusters
* Flexibility in shapes and sizes of clusters
* Able to deal with noise and outliers

### Disadvantages:

* Border points are assigned to whichever clusters find them first
* Faces difficulties in finding clusters of varying densities.   
  _(variation of DBSCAN, HDBSCAN can be used to rectify)_

### Theory:

Epsilon (ε) = Search Distance around a point  
Minimum number of points = min no of points to be classified as a cluster

### Types of Points:

* Noise point : Fails to meet the minimum no of points criteria
* Core Point : Meets the minimum no of points criteria
* Border Point : Is in vicinity of core point and contributing to it, but individually fail to meet the criteria min no of points.

### Validation

Use DBCV (Density Based Cluster Validation) to score DBSCAN. Other validation metrics will mess up the score.

## OPTICS

OPTICS Clustering stands for **Ordering Points To Identify Cluster Structure**. It draws inspiration from the DBSCAN clustering algorithm. It adds two more terms to the concepts of DBSCAN clustering. They are:-

1. **Core Distance:** It is the minimum value of radius required to classify a given point as a core point. If the given point is not a Core point, then it’s Core Distance is undefined.
2. **Reachability Distance:** It is defined with respect to another data point q(Let). The Reachability distance between a point p and q is the maximum of the Core Distance of p and the Euclidean Distance(or some other distance metric) between p and q. Note that The Reachability Distance is not defined if q is not a Core point.

## OPTICS Clustering v/s DBSCAN Clustering:

1. **Memory Cost :** The OPTICS clustering technique requires more memory as it maintains a priority queue (Min Heap) to determine the next data point which is closest to the point currently being processed in terms of Reachability Distance. It also requires more computational power because the nearest neighbour queries are more complicated than radius queries in DBSCAN.
2. **Fewer Parameters :** The OPTICS clustering technique does not need to maintain the epsilon parameter and is only given in the above pseudo-code to reduce the time taken. This leads to the reduction of the analytical process of parameter tuning.
3. This technique does not segregate the given data into clusters. It merely produces a Reachability distance plot and it is upon the interpretation of the programmer to cluster the points accordingly.