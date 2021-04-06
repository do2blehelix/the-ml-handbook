---
title: 'Data Science Project Charter '
description: ''
date: 2020-01-28T00:10:48.000+09:00
weight: "2"

---
# Data Science Project Charter

## 1. Data Gathering

Data Gathering and dictionary creation. Data understanding plays a key role to understand what the data means.

## 2. Exploratory Data Analysis

EDA is divided into 2 phases

### Univariate Analysis

Analyze and understand the ranges and categories of variables and check their distributions.

### Bivariate Analysis

Plot the variables of interest against the dependent variable.

### Correlation

Generate a correlation heatmap to figure out the highly correlated independent variables.

## 3. Data Wrangling

### Clean/Impute Missing Variables

Data with a lot of missing variables generate noise within the model. It is advised to clean the data by either removing the variable if a high proportion of missing values exist.

### Outlier Treatment

Take a call whether to keep the outliers or cap them at a certain level.

### Feature Engineering

Generate new features based on existing variables.

### Standardizing

Standard or Normalize the data to run the model

## 3. Modeling

### Train Test Split

Split the data into training and testing datasets (ideally 70:30)

### Initial Modeling

Run initial model to check for feature importance and prediction accuracy. Run multiple models to check variances across.

### Hyperparameter Tuning

Using grid search run a combination of hyperparameter tuning and check for best results

### Finalize Data and Model

Based on the initial modeling, drop/keep variables of interest/importance and run the final model. 

## Generate Insights

Present the generated insights as a flowing story that connects the business requirement and the data modeling.