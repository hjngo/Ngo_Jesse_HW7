# DSCI 552 — Homework 7

Jesse Ngo

Multi-class, multi-label classification of the UCI Anuran Calls (MFCCs) data with binary relevance (one SVM per label: Family, Genus, Species): Gaussian-kernel one-vs-rest SVMs, L1-penalized linear SVMs, and L1 SVMs with SMOTE, evaluated by exact match, Hamming score and Hamming loss. Then a 50-run Monte Carlo of k-means clustering (k chosen by silhouette) scored against the majority label triplet of each cluster. Also ISLR exercise 12.6.2.

## Structure

```
.
├── README.md
├── .gitignore
├── requirements.txt
├── data
│   ├── Frogs_MFCCs.csv
│   └── Readme.txt
└── notebook
    └── Ngo_Jesse_HW7.ipynb
```

## Running

```
pip install -r requirements.txt
```

Open `notebook/Ngo_Jesse_HW7.ipynb` in Jupyter and run all cells. The data is loaded with the relative path `../data`. The Gaussian SVM grid search (10-fold CV) and the 50-run k-means Monte Carlo are the slow parts.

## Data

Anuran Calls (MFCCs), UCI Machine Learning Repository:
https://archive.ics.uci.edu/ml/datasets/Anuran+Calls+%28MFCCs%29
