---
layout: default
parent: Supervised Learning
title: Time Series / Forecasting
nav_order: 5

---
### Time Series (Forecasting) \[Method = Box-Jenkins (B-J)\]

#### Components

**Trend :** A long term (relatively smooth) pattern that usually persists for more than one year

_Eg : increasing no of flight passengers_

**Seasonal :** Pattern that occurs at regular intervals. \[multiple times in a year (least is once a year)\]

_Eg December sale_

**Cyclical :** Pattern that occurs over a long time, generally continues over a year

_Eg : Recession_

**Random :** The component obtained after the above patterns have been extracted.

#### Models

**White Noise :** Series is purely random in nature (best take average of model)

**AutoRegressive Model :** (p) : Past Terms

No of past values to be taken into account = parameters = no of beta coefficients taken into equation.

_Yt = f ( Yt-1 , Yt-2 , Yt-3 , ….. ε )_

**Moving Average Model :** (q) : Error Terms

Forecast by taking the error terms. The error terms are assumed to be white noise with mean zero and a constant variance.

_Yt = f ( εt-1 , εt-2 , εt-3 , ….. )_

**ARMA Model :** (p,q)

Combines AutoRegressive and Moving Average models

_Y = \[ B0 + B1Yt-1 + B2Yt-2 + B3Yt-3 + εt \] + \[ ϕ0 + ϕ1εt-1 , ϕ2εt-2 , ϕ3εt-3 , ….. εt-q \]_

**ARIMA Model :** (p,d,q)

Combines ARMA with differencing (I)

I = 1 : yt - yt-1 // I = 2 : (yt - yt-1) - (yt-1 - yt-2) _eg: 25, 16, 9, 4 : (25-16) - (16-9) : 9, 7_

_ARIMA (1,0,0) = AR Model ARIMA (0,0,1) = MA Model ARIMA (1,0,1) = ARMA Model ARIMA (0,1,0) = Random walk Model_

Positive auto-correlation to higher lags -> higher order differencing

Zero or negative for first order -> no differencing needed

Optimal order of differencing -> best prediction

**Exponential Smoothing Model :**

Takes the average of the last few observations

#### Stationarity![](https://lh4.googleusercontent.com/P7qQPE2R56lbKYrZQJqKjA-odnrowOTjhbLmasBIUHKvQy5-fyUB1euJXIFp4z8tiRfa5gNOlnoCqFjuB4QNUcZPuWsUju2VuLGF0MjzzUcbnXDn4BMbv6_dX9IhrOzBmVfjOGJx =101.19249841068017x40)

**Stationary Series : In a stationary series the mean variance and autocorrelation are all constant over time.**![](https://lh4.googleusercontent.com/UqUWgR9gRptIANMGTm3Zx9Kh8LPd7wO5lwgENgLywi-AxiC8chLa8fPh4OC2yPr5kwrF1KQVELq8PW3pp2knRuSgqNWVnd_pWFE4QBw2oWwRlNgoMbdeKDBasFoqM3-CIMWMfZNY =150.60944206008583x55)![](https://lh3.googleusercontent.com/gDfimTayxUIEfOGgH6EZNn_G4n5p7lgJ7a6wkkMED_4Ozb4nRVKQhWt2yFyNwt1wZC3R-vYPt_F2x4adCk8Z28I5gcbi7UAA7xnsUCAXEQ_JBMwHlIRuBeNmS1zPbE35kSliXWbb =100.7469670710572x42)

* The mean of the series should not be a function of time. It should be a constant
* The variance of the series should not be a function of time
* The covariance of the i th term and the (i + m) th term should not be a function of time![](https://lh5.googleusercontent.com/KPxuhEbavlyk2wl16xpM-l0GLi_qf6RY73791jSJTL3Oa5H7GUtVCFEk4dxJ4UW0slKGFUIWuSkykKCXKshorir50xORUvlramcLNViXOQZEi1v-3X9eWqBOe6Le8sHbnvrmwFu7 =112.65901060070674x42)

**Types of Stationarity :** Strictly Stationary / Weakly Stationary / Covariance Stationary

A series which is non stationary can be made stationary after differencing (called as Integrated) hence ARIMA is used for non stationary while ARMA for stationary variables.

**Dickey Fuller Test** of stationarity : if null hypothesis is rejected then we get a stationary time series.



![](https://docs.google.com/drawings/u/0/d/sck4Fucjt68q1SJCOeBRq7Q/image?w=222&h=201&rev=278&ac=1&parent=1DFQeQ9FRGL5QV2y-d85pI0R563x5zlvv_Ln5yTr6x-w =222x201)

The estimation and forecasting of univariate time series is carried out by Box-Jenkins (B-J) methodology. It is only applicable to stationary variables.

1. Identification
   1. **AutoCorrelation Function (ACF)** : It measures a simple correlation between current observation (Yt) and the observation (p) periods from the current one (Yt-p) _eg Y5 \~ Y4_
   2. **Partial AutoCorrelation Function (PACF)** : Used to measure the degree of association between Yt and Yt-p with the effects at intermediate time lags removed. _eg Y5 \~ Y1_
   3. Inference from ACF and PACF : To see to what extent the current values of a series are related to past values.

Correlograms are plotted (plot of ACF vs lags) to find the initial values for the order of p & q of the AR and MA process. This is done by looking at the ACF and PACF coefficients and finding the pattern from the table

2. Estimation
   1. Yule Walker Procedure
   2. Method of Moments
   3. Maximum Likelihood Method

3. Diagnostic Checking : Different methods can be obtained for various combinations of AR and MA
   1. **Lowest value of AIC / BIC / SBIC**
   2. **Plot of residual ACF** : should be random / no pattern in error / mean should be zero / residuals should be white noise

1. Check if data is regularly spaced and same intervals
2. Format dates appropriately
3. Sort the dates
4. Check for missing values
   1. proc expand -> interpolate missing values (can also aggregate data)

Original Time Series - Seasonal Component = Seasonally Adjusted
