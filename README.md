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
   - Encoded
