# 08 — Overfitting & Cross-Validation

## Overview

A deep dive into **model evaluation methodology**: why training error alone is misleading, how to properly select hyperparameters, and why cross-validation is essential. Applied to Ridge regression on clothing price prediction.

## What's Inside

- **Custom `train_test_split()`** with seed control for reproducibility
- **Stability analysis**: comparing model variance across 10 different random splits
  - λ=1 → wildly unstable (MSE from 14K to 137K)
  - λ=1000 → stable and consistent
- **Learning curves**: MSE train vs. MSE test across training set sizes (30%–100%)
- **Bias-variance tradeoff visualization**: MSE curves across λ = 0.1 to 10⁹
  - Overfitting zone (small λ): low train error, high test error
  - Underfitting zone (large λ): both errors high
  - Sweet spot: λ ≈ 10⁶
- **Custom k-fold cross-validation**: `cross_validate()` function from scratch
- **Proper hyperparameter selection**: CV on training set only, test set for final evaluation
- **Extreme regularization analysis**: showing how λ → ∞ makes the model predict constants
- **R² as a complementary metric**: detecting "models that do nothing"

## Key Techniques

`Train/Test Split` · `K-Fold Cross-Validation` · `Learning Curves` · `Bias-Variance Tradeoff` · `Regularization Path` · `R² Score` · `Model Selection`

## Results

- Cross-validation selects λ = 10⁶ — same as test-set tuning, but methodologically sound
- At λ = 10¹⁵, MSE looks "good" (8692) but R² ≈ 0 — the model predicts the same value for everything
- MSE alone is insufficient: always pair with R² or residual analysis

## Dataset

**Fashion-MNIST** — 784 pixel features → clothing price prediction

## How to Run

```bash
jupyter notebook overfitting_validation.ipynb
```
