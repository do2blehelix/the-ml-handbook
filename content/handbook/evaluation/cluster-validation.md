---
layout: default
title: "☑️ Cluster Validation Metrics"
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 5
weight: 3

---
# Cluster Validation Metrics

***

Validation is an important part of clustering and our end goal is to get the measure whether the clusters were efficient or not. Efficient clusters have similar data huddled together and have clear separation from other clusters.

**Compactness** : how close the data are to each other **_`(within-cluster-variance)`_**

**Separability** : how far/distinct clusters are from each other **_`(between-cluster-variance)`_**

> Optimum clusters should have **similar data clustered together** `(high compactness)` and **all clusters as far as possible from each other** `(high separability)`

***

## Internal Indices:

Internal Indices measure how good the clusters are in terms of within-cluster-variance and between-cluster-variance. Some of the measures are :

### ⚪ Silhouette Index `[-1 to 1]`

The silhouette index measures the average distance between the clusters. The silhouette index displays a measure of how close each point in one cluster is to points in the neighboring clusters.

\**Range :  
\**1 = Great Score  
0 = Equal distance from both clusters (overlapping clusters)  
\-1 = Misclassified, placed between clusters

    Silhouette Coefficient Si = (b - a) / max(a,b) 
    S = average (S1 , S2 , S3 ……)
    
    a = average distance to other samples in the same cluster
    b = average distance to samples in the closest neighbouring cluster

### ⚪ Calinski-Harabasz

The Calinski-Harabasz index also known as the Variance Ratio Criterion, is the ratio of the sum of **between-clusters dispersion** and of **inter-cluster dispersion** for all clusters, the higher the score , the better the performances.

### ⚪ Davies Bouldin

This index signifies the average ‘similarity’ between clusters, where the similarity is a measure that compares the distance between clusters with the size of the clusters themselves. A lower Davies-Bouldin index relates to a model with better separation between the clusters.

### ⚪ BIC

### ⚪ Dunn Index

Don't use on DBSCAN as noise will lower scores. Also doesn't work well with rings/circular types of points. Works well with compact clusters which are far away from each other.

## External Indices:

They require already applied labels to validate against to find out if the clusters had meaning from already labelled data eg Sales)

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

## Relative Indices

bouldin and calinksi and silhoutte ???