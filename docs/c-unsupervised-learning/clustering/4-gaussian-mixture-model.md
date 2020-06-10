---
layout: default
title: Gaussian Mixture Model
parent: Clustering
grand_parent: Unsupervised Learning
nav_order: 4

---
# Gaussian Mixture Model Clustering

Each point belongs to every cluster, but has a different level of membership. It assumes that each cluster has a certain statistical distribution.

**Expectation - Maximization Algorithm**

### Advantages :

* Soft Clustering, sample members of multiple clusters.
* Cluster shape flexibility. _(cluster can contain another cluster inside of it)_

### Disadvantages :

* Sensitive to initialization values
* Slow convergence rate
* Possible to converge to a local optimum

### Process:

1. Initialize k Gaussian distributions
2. Soft cluster the data into the Gaussian distributions **`(Expectation step)`**
3. Re-estimate the Gaussian **`(Maximization step)`**
4. Evaluate log-likelihood to check for convergence
5. Repeat from Step.2 until convergence