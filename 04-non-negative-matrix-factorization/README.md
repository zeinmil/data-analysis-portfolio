# 04 — Non-Negative Matrix Factorization (From Scratch)

## Overview

Implementation of the **Lee & Seung NMF algorithm** from scratch. Unlike PCA which can produce negative components, NMF decomposes data into purely additive parts — making the components directly interpretable as "building blocks" of images.

## What's Inside

- **Custom `MyNMF` class** implementing the multiplicative update rules:
  - `compute_loss()` — Frobenius norm between original and reconstructed data
  - `initialize_matrices()` — smart random initialization scaled by data mean
  - `update_matrices()` — vectorized Lee & Seung multiplicative updates (no for-loops)
  - `fit_transform()` — full iterative optimization with convergence check
  - `transform()` / `inverse_transform()` — projection and reconstruction
- **Component visualization**: NMF components as interpretable "parts" of clothing
- **Image compression**: NMF vs. PCA reconstruction comparison at 3, 5, 10, 50, 100 components
- **2D projection**: scatter plots colored by true labels and K-Means clusters
- **NMF + K-Means pipeline**: accuracy analysis across different numbers of components

## Key Techniques

`Lee & Seung Algorithm` · `Multiplicative Updates` · `Frobenius Norm` · `Parts-Based Decomposition` · `NMF vs PCA Comparison`

## Results

- NMF components are visually interpretable (e.g., collar shapes, sleeves, pant legs) unlike PCA's ghost-like eigenvectors
- Peak clustering accuracy around 10 NMF components
- NMF captures local features while PCA captures global variance — complementary approaches

## Dataset

**Fashion-MNIST** — 784 pixel features, 3 clothing classes

## How to Run

```bash
jupyter notebook nmf_analysis.ipynb
```
