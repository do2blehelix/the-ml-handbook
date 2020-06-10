---
layout: default
parent: Statistics
title: Dispersion & Spread
nav_order: 2
---

# Measures of Dispersion/Spread
---


|Name | Spread |
|:---|:---|
| **Range** | Max - Min value |
| **Percentile** | Divides the data into `100 equal parts` using 99 points |
| **Decile** | Divides the data into `10 equal parts` using 9 points |
| **Quartile** | Divides the data into `4 equal parts` using 3 points (25%, 50%, 75%)  &nbsp; <br> *Median is the 2nd quartile (50%) . Interquartile range : 25% - 75%* |



```
ℹ Boxplot uses a limit of 1.5 IQR (Inter-Quartile Range) at whiskers to identify outliers
```

---

&nbsp;


## Standard Deviation `σ`

```
 `σ` (population) | `s`  (sample) | Unit = same as data
```

How far are the data dispersed from the mean. How much the members of a group differ from the mean value for the group. sq-root of variance.

![](https://lh6.googleusercontent.com/vrNBhcqa4xn6GtU-0LmBDVuRKosSxe3NHnW1FM758FgYzPNnzP0jukINbQft_N73lmRAK9-F5xq4kjozpG_D5QRZf_06vBzcFqgpvnwta2pMs5OfiZluT-ozTHESyLuZvsnOgCyv)  ![](https://lh5.googleusercontent.com/UKkCzyH5GaYB00yOLoq4D0qcRQN00_qvqV49FGa7qLCKMLN5Hs54urW_9iqCs28yAWGxnlcdbCsqnsAMe_szaDBeAVJUqEUvn3D09-VYjGtfybpSd4GX5VrUG4a5sLPau2g85Zmj)

---



## Variance `σ2`

Indicates how spread out the data are.
```
Unit = data squared
```

- Total Error = Sum of deviances from the mean = ∑ (xi - x̄)
- Sum of squared error (SSE) = ∑ (xi - x̄)2
- Variance = SSE ➗ (n-1) for estimating population
- Variance = SSE ➗ (n)  for sample

---



## Standard Error (of the mean) (SEM)

(using the sample means to estimate the population mean) is the **standard deviation of all sample means** (of a given size). [see Central Limit Theorem]

```
σ  ÷ √n
```

---



## Confidence Interval

```
CI = mean ± [(z-scores for confidence level)*standard error]
```

---



## Z Scores

z is a unit of measure that is equivalent to the number of standard deviations a value is away from the mean value.  

```
Z = (Data Point - Mean) / Standard Deviation Eg : if z = 1.79 , then it is 1.79 σ away from the mean*
```