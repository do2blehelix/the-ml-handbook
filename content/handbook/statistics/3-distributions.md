---
title: "Distributions"
date: 2020-01-30T00:38:25+09:00
description: Distributions
weight: 3

---



# Distributions
___

## Normal / Gaussian / Continuous Distribution

data distributed symmetrically around the center `skewness = kurtosis = 0`. <br>
_Mean = Median = Mode. Also known as the bell curve._

## Binomial Distribution

Discrete distribution used in statistics. Only counts 2 states typically 0 and 1.

## Uniform Distribution

Consists of similar values throughout

## Skewed Distribution

Data distributed which spikes towards either ends as opposed to the central spike in normal distribution (skewness: lack of symmetry)



**Kurtosis : pointiness of the curve**
Positive kurtosis = leptokurtic | Negative kurtosis = platykurtic




Data dist type | Measure of Central Tendency | Measure of spread (variation)
 :---: | :---: | :---:
Normal | Mean | Standard Deviation
Non normal (skewed) | Median | Range, Percentile & IQR




> To convert any dataset with any mean & std deviation to a dataset with mean = 0 & std dev = 1.  
Can be done using z-scores: z = (x - x̄) ÷ s



### Central Limit Theorem

The distribution of the sample means tends towards a normal distribution as the number of samples increase

-   Take a random population and plot its distribution (assuming distribution ≠ normal distribution)
-   Samples of constant size n are to be taken from the population (n1 = n2 = n3 …)
-   Take a random sample of size n1 from the population and calculate its mean x̄1
-   Take a random sample of size n2 from the population and calculate its mean x̄2
-   Plot the means x̄1, x̄2, x̄3 …
-   The sampling distribution (plot of x̄1, x̄2, x̄3 …) tends to be a normal distribution as the number of samples increases
-   The variance of the sampling distribution = The variance of the population / sample size _σx̄2 = σ2 / n_
-   With a higher value of n, the sampling distribution tends to have a lower variance (high kurtosis), and vice-versa
-   The standard deviation of the sampling means is called Standard Error of the Mean.

![](https://lh3.googleusercontent.com/eH7u73SOU6FMMOTbdRfx2JqdESutPfl8ClVYTkk4KLO5_Aq5fP0QvVd4ViWDEZ6rqpIZehKkfa4kAwbN_aM5WnLRPl8N0odC1372kNU5_TokNNaLnHQHOp4pXQbQ1TkjAFpyph8l)![](https://lh3.googleusercontent.com/lIGbfcym_m1t1UMDYmKHJTwxDaBdlKUecB6o0RQ5amQ0lT6VuJAnDjJAoB-SaFQNssE9aPRHJw7_Qt4DgMOsjYfzuhFa3uqiKK5WVLlbcRckudz90njAj4JM0t7E1HY1RSrp8PeN)