# 07 — Linear & Ridge Regression (From Scratch)

## Overview

From classification to **regression**: predicting continuous clothing prices from pixel data. This project implements both ordinary least squares (OLS) and Ridge regression from scratch, exploring why naive linear regression fails on high-dimensional image data and how regularization and dimensionality reduction help.

## What's Inside

- **Custom `MyLinearRegression` class**:
  - `fit()` — normal equations with rank verification (`X^T X` invertibility check)
  - `predict()` — matrix multiplication inference
  - `mse()` — Mean Squared Error
  - `r2()` — R² coefficient of determination
- **Custom `MyRidgeRegression` class** (extends LinearRegression):
  - Regularized normal equations: `w = (X^T X + λI)^{-1} X^T y`
- **Rank deficiency diagnosis**: why OLS fails on 784-dimensional pixel data
- **PCA + Regression pipeline**: projecting to r components before regression
- **Intercept analysis**: dramatic improvement from adding a bias column
- **Lambda tuning**: MSE/R² curves across λ = 0.001 to 1000
- **PCA vs. Ridge comparison**: which approach handles high-dimensional regression better

## Key Techniques

`Normal Equations` · `Ridge Regularization` · `Matrix Rank` · `PCA + Regression` · `Intercept/Bias Term` · `Hyperparameter Tuning`

## Results

- OLS fails (rank deficient matrix — more pixels than independent features)
- Adding an intercept is critical: R² jumps from negative to positive
- Ridge with intercept outperforms PCA + OLS across all configurations
- Optimal λ ≈ 1000 balances bias and variance

## Dataset

**Fashion-MNIST** — 784 pixel features → predict clothing price (continuous target)

## How to Run

```bash
jupyter notebook linear_ridge_regression.ipynb
```
