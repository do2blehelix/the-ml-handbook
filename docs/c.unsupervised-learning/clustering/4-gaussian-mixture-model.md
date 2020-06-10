---
layout: default
title: Gaussian Mixture Model
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 4
---



# Gaussian Mixture Model Clustering

Each point belongs to every cluster, but has a different level of membership. It assumes that each cluster has a certain statistical distribution.
Expectation - Maximization Algorithm
**Advantages :**Soft Clustering, sample members of multiple clusters.Cluster shape flexibility. *(cluster can contain another cluster inside of it)***Disadvantages :**Sensitive to initialization valuesSlow convergence ratePossible to converge to a local optimum

**Process :**Initialize k Gaussian distributionsSoft cluster the data into the gaussian distributions *(Expectation step)*Re-estimate the gaussian *(Maximization step)*Evaluate log-likelihood to check for convergenceRepeat from Step.2 until convergence