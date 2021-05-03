---
title: Distributions
date: 2020-01-30T00:38:25.000+09:00
description: Distributions
weight: 3

---
# Distributions

Now that we've seen the [central point of a distribution](/the-ml-handbook/handbook/statistics/1-central-tendency/), and then the [deviation of data from the central point](the-ml-handbook/handbook/statistics/2-dispersion-spread/), let's explore how these distributions look like.

Before we explore the distributions, its necessary to understand a few key terminologies

## Terminologies

### Skewness

Skewness is the property of the 

* Positive skewed = data is heavy towards the left ; tail towards the right
* Negative skewed = data is heavier towards the right ; tail towards the left

### Kurtosis

Kurtosis simply refers to the pointiness of the curve. The spikier the curve, the more the kurtosis value is.

* Positive kurtosis = leptokurtic
* Negative kurtosis = platykurtic

***

## Normal / Gaussian / Continuous Distribution

data distributed symmetrically around the center `skewness = kurtosis = 0`. <br>
_Mean = Median = Mode. Also known as the bell curve._

**Normal Distribution Data**

| Percentage | μ ± s.d. |
| --- | --- |
| 68.3 % | μ ± 1σ |
| 95.5 % | μ ± 2σ |
| 99.7 % | μ ± 3σ |

## Binomial Distribution

Discrete distribution used in statistics. Only counts 2 states typically 0 and 1.

## Uniform Distribution

Consists of similar values throughout

## Skewed Distribution

Data distributed which spikes towards either ends as opposed to the central spike in normal distribution (skewness: lack of symmetry)

**Kurtosis : pointiness of the curve**
Positive kurtosis = leptokurtic | Negative kurtosis = platykurtic

| Data dist type | Measure of Central Tendency | Measure of spread (variation) |
| :---: | :---: | :---: |
| Normal | Mean | Standard Deviation |
| Non normal (skewed) | Median | Range, Percentile & IQR |

> To convert any dataset with any mean & std deviation to a dataset with mean = 0 & std dev = 1.  
> Can be done using z-scores: z = (x - x̄) ÷ s

### 

***

### Central Limit Theorem

The distribution of the sample means tends towards a normal distribution as the number of samples increase

* Take a random population and plot its distribution (assuming distribution ≠ normal distribution)
* Samples of constant size n are to be taken from the population (n1 = n2 = n3 …)
* Take a random sample of size n1 from the population and calculate its mean x̄1
* Take a random sample of size n2 from the population and calculate its mean x̄2
* Plot the means x̄1, x̄2, x̄3 …
* The sampling distribution (plot of x̄1, x̄2, x̄3 …) tends to be a normal distribution as the number of samples increases
* The variance of the sampling distribution = The variance of the population / sample size _σx̄2 = σ2 / n_
* With a higher value of n, the sampling distribution tends to have a lower variance (high kurtosis), and vice-versa
* The standard deviation of the sampling means is called Standard Error of the Mean.

![](https://lh3.googleusercontent.com/eH7u73SOU6FMMOTbdRfx2JqdESutPfl8ClVYTkk4KLO5_Aq5fP0QvVd4ViWDEZ6rqpIZehKkfa4kAwbN_aM5WnLRPl8N0odC1372kNU5_TokNNaLnHQHOp4pXQbQ1TkjAFpyph8l)![](https://lh3.googleusercontent.com/lIGbfcym_m1t1UMDYmKHJTwxDaBdlKUecB6o0RQ5amQ0lT6VuJAnDjJAoB-SaFQNssE9aPRHJw7_Qt4DgMOsjYfzuhFa3uqiKK5WVLlbcRckudz90njAj4JM0t7E1HY1RSrp8PeN)

***

How Do We Transform Skewed Data?

Since you know how much the skewed data can affect our machine learning model’s predicting capabilities, it is better to transform the skewed data to normally distributed data. Here are some of the ways you can transform your skewed data:

* Power Transformation
* Log Transformation
* Exponential Transformation