# Customer Segmentation using Hierarchical Clustering

This project applies Agglomerative Hierarchical Clustering to segment customers based on behavioral data. The analysis compares multiple linkage strategies and evaluates cluster quality using Silhouette Score and PCA-based visualization.

The goal is to identify meaningful customer groups and determine the most appropriate clustering structure through both quantitative and visual validation.

## Project Overview

Clustering is an unsupervised learning technique used to group similar observations without predefined labels.
---

## Skills Demonstrated

- Unsupervised Machine Learning

- Hierarchical Clustering

- Model Evaluation (Silhouette Analysis)

- PCA for dimensionality reduction

- Experimental comparison of multiple models

- Analytical debugging and validation

- Data visualization and interpretation

---
## Key Findings

- Ward linkage produced the most stable and interpretable clusters.

- Silhouette Score helped identify optimal cluster numbers.

- Visual inspection in PCA space confirmed separation quality.

- Careful tracking of cluster labels ensured correct visualization across experiments.

This project demonstrates the importance of combining:

- Quantitative metrics

- Visual diagnostics

- Careful experimental tracking

- Debugging analytical pipelines

---

## Technologies Used

- Python

- Pandas

- NumPy

- Scikit-learn

- Matplotlib

- Seaborn


In this project, I:

- Standardized numerical features

- Applied Agglomerative Clustering

- Compared multiple linkage methods:

  - Ward
        
  - Complete
        
  - Average
        
  - Single

- Evaluated clustering performance using Silhouette Score

- Visualized clusters using Principal Component Analysis (PCA)

- Selected the best-performing clustering configurations for interpretation


## Methodology
1️ Data Preprocessing

- Feature scaling using standardization

- Preparation of model input matrix:
```
X = data_standardized
```

2️ Hierarchical Clustering

For:

- Number of clusters: 2–10

- Linkage methods: Ward, Complete, Average, Single

Each model:

- Was fitted using AgglomerativeClustering

- Evaluated using Silhouette Score

Stored together with cluster labels for reproducible comparison
```
results.append({
    "num_of_clusters": n_clusters,
    "linkage": linkage,
    "silhouette_score": score,
    "labels": labels
})
```
Storing cluster labels enabled accurate visualization and prevented inconsistencies when comparing models.

3️ Model Evaluation

Clustering performance was evaluated using:

- Silhouette Score (quantitative assessment)

- PCA visualization (qualitative inspection)

The four best-performing Ward-linkage models were selected and visualized for comparison.


## Project Structure
```
.
├── Customer Segmentation.ipynb
├── README.md
└── shopping_centre.csv
```

# How to Run

Clone the repository:
```
git clone https://github.com/dieeju7/Customer-Segmentation.git
```

Install dependencies:
```
pip install pandas numpy scikit-learn matplotlib seaborn
```
Launch Jupyter Notebook: Customer Segmentation.ipynb

