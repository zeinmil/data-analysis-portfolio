# 02 — K-Means Clustering (From Scratch)

## Overview

Full implementation of the **K-Means clustering algorithm** (Lloyd's algorithm) from scratch using only NumPy. Applied to the Fashion-MNIST dataset (784-pixel grayscale images of clothing) to discover natural groupings without labels.

## What's Inside

- **Custom `MyKMeans` class** built incrementally via monkey-patching:
  - `random_centroids()` — random initialization from data points
  - `assign_clusters()` — vectorized Euclidean distance computation
  - `update_centroids()` — mean recalculation per cluster
  - `fit()` — full Lloyd's algorithm with convergence tolerance
  - `predict()` — classify new data points
- **Visual evaluation**: centroid images showing what each cluster "looks like"
- **Contingency table analysis**: comparing clusters vs. true labels (T-shirt, Pants, Dress)
- **Accuracy vs. number of clusters**: testing with k = 2, 4, 8, 10, 15

## Key Techniques

`Lloyd's Algorithm` · `Euclidean Distance` · `Vectorized NumPy` · `Contingency Tables` · `Heatmaps (Seaborn)`

## Results

The algorithm successfully separates the 3 clothing categories with increasing accuracy as the number of clusters grows — demonstrating how splitting into sub-clusters captures intra-class variability.

## Dataset

**Fashion-MNIST** — 784 pixel features per image, 3 clothing classes (T-shirt, Pants, Dress)

## How to Run

```bash
jupyter notebook kmeans_clustering.ipynb
```

> **Note**: Requires `pixels.csv` and `labels.csv` data files. Originally developed on Google Colab.
