# 📊 Data Analysis & Machine Learning — From Scratch

A collection of 9 projects covering the full data analysis pipeline: from raw data cleaning to supervised learning models, with most algorithms **implemented from scratch** in Python/NumPy.

Built during my studies at **PSL University** (Paris Sciences & Lettres), these projects progressively tackle unsupervised learning, dimensionality reduction, classification, regression, and model evaluation — all applied to real datasets including **Fashion-MNIST** (clothing images, 784 pixels) and **superconductivity data** (81 physical features).

---

## 🗂️ Projects

### Unsupervised Learning & Dimensionality Reduction

| # | Project | Key Techniques | Dataset |
|---|---------|---------------|---------|
| 01 | [Data Preprocessing](./01-data-preprocessing) | Pandas, cleaning, type conversion, pixel extraction | Clothes e-commerce CSV |
| 02 | [K-Means Clustering](./02-kmeans-clustering) | Lloyd's algorithm (from scratch), centroid visualization | Fashion-MNIST (784px) |
| 03 | [Principal Component Analysis](./03-principal-component-analysis) | Eigendecomposition, variance explained, image compression (from scratch) | Fashion-MNIST |
| 04 | [Non-Negative Matrix Factorization](./04-non-negative-matrix-factorization) | Lee & Seung multiplicative updates (from scratch) | Fashion-MNIST |
| 05 | [MDS & Isomap](./05-mds-and-isomap) | Multidimensional Scaling, geodesic distances, manifold learning (from scratch) | Fashion-MNIST |

### Supervised Learning

| # | Project | Key Techniques | Dataset |
|---|---------|---------------|---------|
| 06 | [KNN Classification](./06-knn-classification) | K-Nearest Neighbors (from scratch), confusion matrix | Fashion-MNIST (10 classes) |
| 07 | [Linear & Ridge Regression](./07-linear-and-ridge-regression) | OLS, Ridge regularization, PCA + regression (from scratch) | Fashion-MNIST + prices |
| 08 | [Overfitting & Cross-Validation](./08-overfitting-and-cross-validation) | Train/test split, k-fold CV, learning curves, bias-variance tradeoff | Fashion-MNIST + prices |

### End-to-End Project

| # | Project | Key Techniques | Dataset |
|---|---------|---------------|---------|
| 09 | [Superconductivity Prediction](./09-superconductivity-prediction) | Full pipeline: EDA → PCA/Isomap visualization → Ridge regression → evaluation | Superconductivity (81 features) |

---

## 🛠️ Tech Stack

- **Python** — NumPy, Pandas, Matplotlib, Seaborn
- **Scikit-learn** — used for comparison/validation (most algorithms are coded from scratch)
- **Google Colab** — original development environment

## 🧠 What Makes This Different

Most algorithms are **not just called from sklearn** — they are **implemented from scratch** using NumPy to understand the underlying mathematics:

- **K-Means**: Lloyd's algorithm with custom centroid initialization and convergence detection
- **PCA**: Eigendecomposition of covariance/correlation matrices, transform & inverse transform
- **NMF**: Lee & Seung multiplicative update rules with Frobenius norm loss
- **MDS**: Double centering of distance matrices + spectral decomposition
- **Isomap**: k-nearest neighbor graph + shortest path (geodesic) distances + MDS
- **KNN**: Cross-distance matrix computation + majority voting
- **Linear Regression**: Normal equations with rank verification
- **Ridge Regression**: Regularized normal equations with lambda tuning

---

## 📁 Repository Structure

```
data-analysis-portfolio/
├── README.md
├── 01-data-preprocessing/
│   ├── README.md
│   └── data_preprocessing.ipynb
├── 02-kmeans-clustering/
│   ├── README.md
│   └── kmeans_clustering.ipynb
├── 03-principal-component-analysis/
│   ├── README.md
│   └── pca_analysis.ipynb
├── 04-non-negative-matrix-factorization/
│   ├── README.md
│   └── nmf_analysis.ipynb
├── 05-mds-and-isomap/
│   ├── README.md
│   └── mds_isomap.ipynb
├── 06-knn-classification/
│   ├── README.md
│   └── knn_classification.ipynb
├── 07-linear-and-ridge-regression/
│   ├── README.md
│   └── linear_ridge_regression.ipynb
├── 08-overfitting-and-cross-validation/
│   ├── README.md
│   └── overfitting_validation.ipynb
└── 09-superconductivity-prediction/
    ├── README.md
    └── superconductivity_prediction.ipynb
```

## 👤 Author

**Zein Miled** — PSL University
