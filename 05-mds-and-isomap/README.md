# 05 — MDS & Isomap: Manifold Learning (From Scratch)

## Overview

Implementation of two non-linear dimensionality reduction methods from scratch: **Multidimensional Scaling (MDS)** and **Isomap**. While PCA and NMF assume linear relationships, these techniques preserve the true geometric structure of data — particularly useful when data lies on a curved manifold.

## What's Inside

- **Custom `MyMDS` class**:
  - `distances()` — efficient pairwise Euclidean distance matrix (vectorized)
  - `double_centre()` — Gram matrix reconstruction from distances
  - `get_principal_components()` — spectral decomposition for embedding
  - `fit_transform()` — complete MDS pipeline
- **Custom `MyIsomap` class**:
  - k-nearest neighbor graph construction
  - Geodesic distance approximation via shortest paths (Dijkstra)
  - MDS on the geodesic distance matrix
- **MDS vs. PCA comparison**: verifying equivalence on linear data
- **Isomap parameter study**: impact of number of neighbors (k = 3, 5, 10, 35, 45)
- **Combined pipeline**: NMF + Isomap visualization — using Isomap to reveal non-linear structure in NMF-projected space

## Key Techniques

`Distance Matrices` · `Double Centering` · `Geodesic Distances` · `k-NN Graph` · `Shortest Path (Dijkstra)` · `Spectral Decomposition` · `NMF + Isomap Pipeline`

## Results

- MDS and PCA produce identical results on this dataset (confirming correctness — both are linear)
- Isomap with small k (3–5) best preserves local cluster structure, achieving ~87% clustering accuracy
- Isomap reveals non-linear separability invisible to PCA/MDS in the NMF-projected space

## Dataset

**Fashion-MNIST** — 784 pixel features, 3 clothing classes

## How to Run

```bash
jupyter notebook mds_isomap.ipynb
```
