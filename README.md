# P2_Unsupervised-Learning_Iris-Data
Iris clustering using K-Means, GMM, and DBSCAN

# Iris Clustering

## 1. Project Overview

This project explores unsupervised learning techniques
to identify patterns and clusters in the Iris dataset.

Three clustering algorithms are implemented and compared:
- K-Means
- Gaussian Mixture Model (GMM)
- DBSCAN

The main objective is to understand how different
clustering algorithms group data and evaluate their
performance using internal clustering metrics.

## 2. Dataset

The Iris dataset contains:
- 150 observations
- 4 numerical features
- 3 flower species

Features:
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The species labels are not used during model training.
They are used only for post-clustering interpretation.

## 3. Methodology

The project follows these steps:

1. Exploratory Data Analysis (EDA)
2. Data preprocessing
3. Feature scaling using StandardScaler
4. Model implementation
5. Parameter experimentation
6. Model evaluation and comparison

## 4. Clustering Algorithms

### K-Means
K-Means partitions observations into a predefined
number of clusters by minimizing within-cluster
sum of squares.

### Gaussian Mixture Model (GMM)
GMM models the data as a mixture of Gaussian
distributions and assigns observations based on
probabilistic membership.

### DBSCAN
DBSCAN identifies clusters based on data density.
It can detect noise and does not require the number
of clusters to be specified in advance.

## 5. Evaluation Metrics

The following internal evaluation metrics are used:

- Silhouette Score: Measures how well observations
  fit within their assigned clusters.
- Davies-Bouldin Index: Measures cluster similarity.
  Lower values indicate better separation.
- Calinski-Harabasz Index: Compares between-cluster
  dispersion with within-cluster dispersion.
  Higher values generally indicate better-defined clusters.

## 6. Results & Comparison

| Model | Clusters | Noise | Silhouette | Davies-Bouldin | Calinski-Harabasz |
|---|---:|---:|---:|---:|---:|
| K-Means | 3 | 0 | 0.4599 | 0.8335 | 241.90 |
| GMM | 3 | 0 | 0.4751 | 0.8867 | 141.23 |
| DBSCAN (eps=0.8) | 2 | 4 | 0.5979 | 0.5688 | 277.65 |

Note: DBSCAN metrics are calculated after excluding
noise points. Therefore, the results are not
perfectly comparable across all models.

## 7. Key Findings

- K-Means and GMM were configured to produce
  three clusters.
- DBSCAN with eps=0.8 identified two clusters
  and four noise points.
- The algorithms produce different clustering
  structures because they use different approaches.
- Internal evaluation metrics provide useful
  comparisons but do not establish the real-world
  meaning of clusters.
