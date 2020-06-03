---
layout: default
parent: Unsupervised Learning
title: Clustering
nav_order: "1"

---
# Clustering

Is a set of data driven partitioning techniques designed to group a collection of objects into clusters.

**⭐ Clustering is finding borders between groups  
⭐ Segmentation is using borders to form groups**

Linkage method

Variance method

Centroid method

**Applications :**

* Market Segmentation
* Sales segmentation : what type of customer wants what
* Credit risk
* Operations : High performing persons and promotions
* Insurance : identifying groups with high average claim cost
* Data reduction : grouping observations to reduce number is obs

The decision of merging two clusters is taken on the basis of closeness of these clusters. There are multiple metrics for deciding the closeness of two clusters :

* Euclidean distance: ||a-b||2 = √(Σ(ai-bi))
* Squared Euclidean distance: ||a-b||22 = Σ((ai-bi)2)
* Manhattan distance: ||a-b||1 = Σ|ai-bi|
* Maximum distance:||a-b||INFINITY = maxi|ai-bi|
* Mahalanobis distance: √((a-b)T S-1 (-b)) {where, s : covariance matrix}

**How to build clusters :**

Select distance measure > Select clustering algorithm > Define the distance between 2 clusters >

Determine no of clusters > Validate the analysis

**Data should ALWAYS be continuous and standardized in nature.**

### K means \[Non Hierarchical\]

It is based on division of objects into non overlapping subsets. Main objective is to form clusters that are homogeneous in nature and heterogeneous to each other. Only for continuous variables.

**Advantages:**

* **Faster, more reliable, works with large data.**
* Computationally lighter than other methods

**Disadvantages:**

* Can only identify clusters circular / spherical in nature. _(check crescent dataset)_
* Distance based

**Process :**

1. Identify value of _‘k’_
2. Assign random k observations as seeds
3. Assign each record to one of the k seeds based on proximity
4. Form clusters
5. Calculate centroids of clusters
6. Assign centroids as new seed
7. Form new clusters
8. Recalculate clusters
9. Continue process until stable clusters are formed (boundary ceases to change)

**Elbow Criterion (Scree Plot):**![](https://lh5.googleusercontent.com/VgUz4jopV1BT6doFeT_UOv2Iao0kbY6Ij6ErVBweUUjoQcTSfdA1AbwNcAToMZRo3yZgcEnMtrrDPY6UzniG5Oec_-otvyy7_w7SmeSpKy3AnxH3NHQq4U90uftzY254_OCS5fZr =247x126)

K means clustering doesn't provide an estimate of the number of clusters required. Hence elbow criterion is used to determine optimal number of clusters.

The method says that you should choose a number of clusters so that adding another cluster does not add any sufficient information. It is plotted by **ratio of within cluster variance to between cluster variance** against number of clusters. The objective is to minimise the within and maximise the between distances.

**Validation :**

* R squared : R2 = Between sum of squares / total sum of squares
* Pseudo f
* Clc
* Silhouette
* pc plot
* ccc cluster criterion

[Visual Example](https://www.naftaliharris.com/blog/visualizing-k-means-clustering/)

### Hierarchical Clustering

Set of nested clusters organized as a hierarchical tree. No decision about number of clusters

It is not used when data is big due to higher processing time.

**Advantages :**

* Produces an additional ability to visualize
* Potent esp if the data contains real hierarchical relationships _(eg evolution)_

**Disadvantages :**

* Computationally intensive
* Sensitive to noise and outliers

**Types :**

* Agglomerative : Start from _n_ clusters and get to _one_ cluster (Bottom up approach)
* Divisive : Start from _one_ cluster and get to _n_ clusters (Top down approach)

**Distance Between Clusters** (Agglomerative Clustering)

* Single link : Shortest distance between an element in one cluster and an element in another cluster.
* Complete link : Largest distance between elements in two clusters. Produces compact clusters.
* Average link : Average distance of elements between 2 clusters.
* Centroid : Distance between the centroids of 2 clusters
* Metroid : Distance between centrally located object in both clusters.
* Ward’s method : Minimize variance between 2 clusters.

  
  
![](https://lh5.googleusercontent.com/jC8mI4S66hPh4i3tr-QZgKZDkkZPrhh0sGcczx2x1BVWLgA0lfXTAH5ncDKa1HkHelh5tfwBASLD3puoEnFb_iOA3LxYpm7MlV8Lqsd-F2BElXVDV0HEVMZEB84QjCRjGdpOS2YS =326x205)

The results of hierarchical clustering can be shown using dendrogram.

1. At the bottom, we start with n data points (observations), each assigned to separate clusters
2. Two closest clusters are then merged till we have just one cluster at the top
3. The height in the dendrogram at which two clusters are merged represents the distance between two clusters in the data space.

The best choice of the no. of clusters is the no. of vertical lines in the dendrogram cut by a horizontal line that can transverse the maximum distance vertically without intersecting a cluster.

### Density Based Spatial Clustering of Applications with Noise _(DBSCAN)_

Clusters densely packed points and labels the other points as noise

**Advantages :**

* No specification of no of clusters
* Flexibility in shapes and sizes of clusters
* Able to deal with noise and outliers

**Disadvantages :**

* Border points are assigned to whichever clusters find them first
* Faces difficulties in finding clusters of varying densities. _(variation of DBSCAN, HDBSCAN can be used to rectify)_

Epsilon (ε) = Search Distance around a point

Minimum number of points = min no of points to be classified as a cluster

**Types of Points:**

* Noise point : Fails to meet the minimum no of points criteria
* Core Point : Meets the minimum no of points criteria
* Border Point : Is in vicinity of core point and contributing to it, but individually fail to meet the criteria min no of pts

Use DBCV (Density Based Cluster Validation) to score DBSCAN. Other validation metrics will mess up the score.

[Visualizing DBSCAN](https://www.naftaliharris.com/blog/visualizing-dbscan-clustering/)

### Gaussian Mixture Model Clustering

Each point belongs to every cluster, but has a different level of membership. It assumes that each cluster has a certain statistical distribution.

Expectation - Maximization Algorithm

**Advantages :**

* Soft Clustering, sample members of multiple clusters.
* Cluster shape flexibility. _(cluster can contain another cluster inside of it)_

**Disadvantages :**

* Sensitive to initialization values
* Slow convergence rate
* Possible to converge to a local optimum

**Process :**

1. Initialize k Gaussian distributions
2. Soft cluster the data into the gaussian distributions _(Expectation step)_
3. Re-estimate the gaussian _(Maximization step)_
4. Evaluate log-likelihood to check for convergence
5. Repeat from Step.2 until convergence

## Cluster Validation

**Types :**

* External Indices (to find out if the clusters had meaning from already labelled data eg Sales)
* Internal Indices
* Relative Indices

**Compactness** : how close the data are to each other _(within cluster variance)_

**Separability** : how far/distinct clusters are from each other _(between cluster variance)_

Optimum cluster should have high compactness and high spearability.

#### External Indices:

They require already applied labels to validate against

* Adjusted Rand Score \[-1 to 1\]
* Fawlks and Mallows \[0 to 1\]
* NMI Measure \[0 to 1\]
* Jaccard \[0 to 1\]
* F-measure \[0 to 1\]
* Purity \[0 to 1\]

Rand Index (Rand Score) = (a + b) / (n)

_a = no of pairs same in both labelled and predicted cluster_

_b = no of pairs different in either labelled or predicted cluster_

_n = no of points_

#### Internal Indices:

* Silhouette Index \[-1 to 1\]
* Calinski-Harabasz
* BIC
* Dunn Index

Silhouette Coefficient Si = (b - a) / max(a,b) S = average (S1 , S2 , S3 ……)

_a = average distance to other samples in the same cluster_

_b = average distance to samples in the closest neighbouring cluster_

Don't use on DBSCAN as noise will lower scores. Also doesn't work well with rings/circular types of points. Works well with compact clusters which are far away from each other.