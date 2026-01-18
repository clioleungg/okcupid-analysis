# OKCupid Profile Clustering  
### Identifying User Archetypes with Agglomerative Hierarchical Clustering

**Authors:** Clio Leung & Paige  
**Course Project:** Unsupervised Learning / Clustering Analysis

---

## 📌 Project Overview

This project applies **agglomerative hierarchical clustering** to online dating profiles from OKCupid to identify meaningful user segments based on **lifestyle behavior** and **socioeconomic status**.

**Goal:**  
Identify distinct, interpretable user archetypes that capture behavioral and income-based differences among users.

**Dataset:**  
- OKCupid profiles dataset  
- ~383 users after data cleaning  

**Final Output:**  
- 3 primary user clusters  
- 1 small outlier cluster  

---

## 🧠 Methodology Summary

### Chosen Features
We selected two variables for clustering:

1. **Unhealthy Score**
   - Composite metric derived from:
     - Drinking habits
     - Smoking habits
     - Drug usage
   - Encoded numerically and normalized to a 0–1 scale

2. **Income**
   - Converted to numeric values
   - Missing values filled with the median
   - Standardized for clustering

**Why these features?**
- Unhealthy score captures **social behavior & lifestyle**
- Income captures **socioeconomic status**
- This combination produced the clearest and most distinct clusters compared to other tested variables (e.g., age, height)

---

## 🔍 Clustering Approach

### Algorithm
- **Agglomerative Hierarchical Clustering**
- **Complete Linkage**

### Why Agglomerative Clustering?
- Dataset size is relatively small
- Many original variables are categorical
- Does not assume spherical clusters
- Allows for hierarchical user groupings
- Deterministic (same result every run)
- Handles uneven cluster sizes well

### Why Complete Linkage?
- Measures the **maximum distance** between clusters
- Produces tighter, more compact clusters
- Reduces chaining effects
- Provides better separation than single linkage

---

## 🌲 Determining the Number of Clusters

Using the dendrogram:
- A large jump in merge distance occurs between **4 → 3 clusters**
- We selected **4 clusters** as optimal
- One cluster is treated as an **outlier group**

---

## 🧩 Final Clusters

Each user profile is assigned to one of the following clusters:

| Cluster Name | Description |
|-------------|------------|
| **Wild, Low-Income** | High unhealthy score, lower income |
| **Chill, High-Income** | Low unhealthy score, higher income |
| **Chill, Low-Income** | Low unhealthy score, lower income |
| **Balanced Social Outliers** | Small outlier group with balanced behavior |

---

## 📊 Analysis & Visualizations

The project includes the following visual outputs:

- **Dendrogram** showing hierarchical cluster structure
- **Scatter Plot**
  - X-axis: Unhealthy Score
  - Y-axis: Income
  - Each color represents a cluster
  - Cluster centroids marked with red “X”
- **Bar Charts**
  - Average unhealthy score per cluster
  - Average income per cluster

Cluster centroids are computed by averaging:
- Unhealthy score
- Income  
within each cluster.

---

## 🧪 Files Included

- `profiles-1.xlsx` – Raw OKCupid dataset  
- `clustering.ipynb` – Full data cleaning, clustering, and visualization workflow  
- `README.md` – Project overview and documentation  

---

## 🛠️ Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`
- `scipy`

---

## 🚀 Key Takeaways

- Behavioral lifestyle metrics combined with income can reveal clear user archetypes
- Agglomerative clustering is effective for small, mixed-type datasets
- Complete linkage improves separation and interpretability
- Hierarchical methods provide strong visual intuition via dendrograms

---

## 📎 Notes

This project was completed for academic purposes and demonstrates:
- Feature engineering
- Unsupervised learning
- Clustering evaluation
- Visual interpretation of results

