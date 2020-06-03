---
layout: default
title: Cluster Validation
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 5
---



# Cluster Validation


**Types :**External Indices (to find out if the clusters had meaning from already labelled data eg Sales)Internal IndicesRelative Indices
**Compactness** 	: how close the data are to each other *(within cluster variance)***Separability** 	: how far/distinct clusters are from each other *(between cluster variance)*
Optimum cluster should have high compactness and high spearability.


External Indices:They require already applied labels to validate against
Adjusted Rand Score [-1 to 1]Fawlks and Mallows [0 to 1]NMI Measure [0 to 1]Jaccard [0 to 1]F-measure [0 to 1]Purity [0 to 1]

Rand Index (Rand Score) = (a + b) / (n)*a = no of pairs same in both labelled and predicted cluster**b = no of pairs different in either labelled or predicted cluster**n = no of points*

Internal Indices:Silhouette Index [-1 to 1]Calinski-HarabaszBICDunn Index

Silhouette Coefficient  Si = (b - a) / max(a,b)	S = average (S1 , S2 , S3 ……)*a = average distance to other samples in the same cluster**b = average distance to samples in the closest neighbouring cluster*Don't use on DBSCAN as noise will lower scores. Also doesn't work well with rings/circular types of points. Works well with compact clusters which are far away from each other.