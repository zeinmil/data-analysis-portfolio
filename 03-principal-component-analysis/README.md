# 03 — Principal Component Analysis (From Scratch)

## Overview

Complete implementation of **PCA** from scratch — both on the covariance matrix (centered data) and the correlation matrix (standardized data). Applied to Fashion-MNIST for dimensionality reduction, image compression, and improved clustering.

## What's Inside

- **Custom `MyPCA` class** with full pipeline:
  - `prepare_data()` — centering and optional standardization
  - `compute_comatrix()` — covariance/correlation matrix computation
  - `get_principal_components()` — eigendecomposition and component selection
  - `fit()`, `transform()`, `inverse_transform()` — standard sklearn-like API
- **Variance explained analysis**: cumulative variance curve for 1–100 components
- **Image compression**: visual comparison of reconstructions at 1, 3, 5, 10, 25, 50, 75, 100 components
- **2D scatter plots**: PCA projections colored by true labels and K-Means clusters
- **PCA + K-Means pipeline**: accuracy analysis combining dimensionality reduction with clustering
- **Standardized vs. non-standardized PCA**: comparison and interpretation

## Key Techniques

`Eigendecomposition` · `Covariance Matrix` · `Correlation Matrix` · `Explained Variance` · `Image Reconstruction` · `PCA + K-Means Pipeline`

## Results

- 50 components capture most of the variance while compressing data by ~15x
- PCA projection before K-Means improves clustering speed without significant accuracy loss
- Standardized PCA produces more balanced projections but less sharp reconstructions (expected for homogeneous pixel data)

## Dataset

**Fashion-MNIST** — 784 pixel features, 3 clothing classes

## How to Run

```bash
jupyter notebook pca_analysis.ipynb
```
