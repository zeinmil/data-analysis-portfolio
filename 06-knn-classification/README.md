# 06 — K-Nearest Neighbors Classification (From Scratch)

## Overview

Transition from unsupervised to **supervised learning** with a full KNN implementation from scratch. Applied to the complete Fashion-MNIST dataset (10 classes of clothing) for multi-class classification.

## What's Inside

- **Custom `MyKNN` class**:
  - `cross_distance()` — efficient distance matrix between train and test sets (vectorized)
  - `fit()` — store training data (lazy learning)
  - `predict()` — k-nearest neighbor majority voting with `np.argsort`
  - `score()` — accuracy computation
- **Confusion matrix**: heatmap visualization showing per-class performance
- **Training size impact**: accuracy curve from 50 to 8000 training examples
- **Error analysis**: visualizing misclassified images alongside their k nearest neighbors

## Key Techniques

`K-Nearest Neighbors` · `Euclidean Distance` · `Majority Voting` · `Confusion Matrix` · `Train/Test Split` · `Learning Curves`

## Results

- ~80% accuracy on 10-class Fashion-MNIST with k=5 and 80% train split
- Performance plateaus around 4000–6000 training examples
- Common confusions: shirts vs. T-shirts, coats vs. pullovers (visually similar categories)

## Dataset

**Fashion-MNIST (full)** — 10,000 images, 784 pixels, 10 classes: T-shirt, Pants, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle Boot

## How to Run

```bash
jupyter notebook knn_classification.ipynb
```
