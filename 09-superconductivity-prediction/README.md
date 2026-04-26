# 09 — Superconductivity: Critical Temperature Prediction

## Overview

An **end-to-end data science project** applying all techniques from the portfolio to a real physics problem: predicting the critical temperature of superconducting materials from 81 physical/chemical features.

## What's Inside

### 1. Exploratory Data Analysis
- Dataset overview: 21,000+ superconductors with 81 features
- Distribution analysis: heavy skew toward low critical temperatures
- Statistical summaries and feature inspection

### 2. Visualization (Dimensionality Reduction)
- **PCA** (standardized): 2D projection colored by critical temperature
  - First 2 components explain ~49% of variance
  - Components are a mix of all features (no single dominant feature)
- **Isomap**: non-linear 2D embedding for comparison
- Method selection rationale: PCA and Isomap for projection vs. K-Means for clustering

### 3. Predictive Modeling
- Train/test split (80/20) with proper evaluation methodology
- **Ridge Regression**: hyperparameter tuning via cross-validation
- Feature standardization before modeling
- R² and MSE evaluation on held-out test set

## Key Techniques

`EDA` · `Feature Standardization` · `PCA` · `Isomap` · `Ridge Regression` · `Cross-Validation` · `Train/Test Split`

## Dataset

**Superconductivity Dataset** — 21,263 materials, 81 physical features, target = critical temperature (Kelvin)

Features include atomic mass, density, electron affinity, thermal conductivity, and other material properties.

## How to Run

```bash
jupyter notebook superconductivity_prediction.ipynb
```

> **Note**: Requires the `superconductivity_data.csv` file.
