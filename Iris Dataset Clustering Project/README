# 🌸 Iris Dataset Clustering Project

This project explores **unsupervised learning** techniques to discover natural groupings in the **Iris dataset** using three major clustering algorithms:

- **K-Means Clustering**
- **Hierarchical Agglomerative Clustering**
- **DBSCAN (Density-Based Spatial Clustering)**

---

## 📊 Project Overview

The Iris dataset contains 150 samples of iris flowers with four features:
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The goal is to **cluster the flowers** without using their species labels (`unsupervised learning`), and then evaluate how well the clustering corresponds to the actual species.

---

## 🔧 Techniques Used

### ✅ Data Preprocessing
- Loaded dataset from `sklearn.datasets`
- Scaled features using `StandardScaler`
- Removed label column (`species`) for unsupervised training

### ✅ Exploratory Data Analysis (EDA)
- Pairplots and heatmaps to understand feature relationships
- PCA used for dimensionality reduction and visualization

### ✅ Clustering Algorithms
1. **K-Means**
   - Elbow method used to find optimal `k`
   - Cluster visualization via PCA
2. **Hierarchical Clustering**
   - Dendrogram plotted to choose number of clusters
   - AgglomerativeClustering applied
3. **DBSCAN**
   - Used `k-distance graph` to determine `eps`
   - Detected arbitrary-shaped clusters and noise

---

## 📈 Evaluation Metrics

Although clustering is unsupervised, we evaluated performance by comparing cluster assignments to true labels using:

- **Adjusted Rand Index (ARI)**
- **Confusion Matrix** (visual inspection)
- **PCA plots** of clustered data

### 🔢 Final ARI Scores:

| Algorithm      | Adjusted Rand Index |
|----------------|---------------------|
| K-Means        | 0.5681              |
| Hierarchical   | 0.6153              |
| DBSCAN         | 0.5518              |

---

## 📌 Results & Insights

- **Hierarchical Clustering** performed best among the three, achieving the highest ARI.
- **K-Means** also performed well with proper `k` tuning and scaling.
- **DBSCAN** required fine-tuning of `eps` and `min_samples`, but effectively identified noise and dense clusters.



