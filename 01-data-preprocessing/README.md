# 01 — Data Preprocessing & Cleaning

## Overview

First step of any data analysis pipeline: transforming a raw e-commerce CSV into clean, ML-ready NumPy arrays. This project tackles a **clothing dataset** with product IDs, prices, warehouse origins, and 784-pixel grayscale images stored as strings.

## What's Inside

- **Duplicate detection & removal** based on product IDs
- **String-to-numeric conversion** (price column with `€` symbols)
- **Feature engineering**: extracting warehouse origin (Amsterdam/Berlin) from ID prefixes
- **Pixel extraction**: splitting a single string column into 784 numeric pixel columns
- **Data validation**: detecting corrupted values (NaN, out-of-range pixels)
- **Export to NumPy**: converting clean DataFrames into `uint8` and `float32` arrays

## Key Techniques

`Pandas` · `NumPy` · `str.split()` · `pd.to_numeric` · `groupby` · `boolean masking` · `dtype optimization`

## Dataset

| Feature | Description |
|---------|-------------|
| `id` | Product identifier with warehouse prefix (AM-xxx, BER-xxx) |
| `prix` | Price as string with € symbol |
| `image` | 784 pixel values as a single space-separated string |

## How to Run

```bash
jupyter notebook data_preprocessing.ipynb
```

> **Note**: The notebook was originally developed on Google Colab. You may need to adjust file paths for local execution.
