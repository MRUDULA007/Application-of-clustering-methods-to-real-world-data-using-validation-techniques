---
# Project 2:
## 📊 Clustering Analysis Results

This project applies **K-Means** and **Hierarchical Clustering** to real-world socio-economic data, using multiple validation techniques.

### 🗂 Dataset
- **Source:** `World Indicators.csv`
- Key features: Birth Rate, GDP, Health Expenditure, Internet Usage, Life Expectancy, Mobile Phone Usage, Population Distribution, etc.

---

### 🔹 Number of Clusters Identified
- **K-Means:** 4 clusters
- **Hierarchical Clustering:** 2 clusters

---

### 📈 Performance Metrics

| Metric                   | K-Means  | Hierarchical |
|--------------------------|----------|--------------|
| **Dunn Index**           | 0.1666   | 0.0907       |
| **Silhouette Score**     | 0.5687   | 0.5800       |
| **Davies–Bouldin Score** | 0.5168   | 0.5637       |
| **Calinski–Harabasz**    | 579.39   | 361.60       |

---

### 🌍 Country Groupings

#### **K-Means Clusters**
- **Cluster 1:** Botswana, Gabon, Libya, Singapore, Finland, Italy, Kuwait, Oman, Saudi Arabia, Argentina, Uruguay, etc.  
- **Cluster 2:** Angola, Burkina Faso, Chad, Ethiopia, Myanmar, Yemen, Haiti, etc.  
- **Cluster 3:** Algeria, Benin, India, Pakistan, France, Canada, United States, Turkey, Mexico, etc.  
- **Cluster 4:** Egypt, Morocco, South Africa, Japan, Australia, Germany, Brazil, Peru, etc.

#### **Hierarchical Clusters**
- **Cluster 1:** Algeria, Botswana, Egypt, India, Canada, United States, etc. (113 countries)  
- **Cluster 2:** Angola, Benin, Chad, Haiti, Mexico, Nicaragua, etc. (73 countries)

---

### 📊 Visualizations
- Scatter plots of Infant Mortality Rate vs Mobile Phone Usage for each cluster.
- Comparative plots for K-Means and Hierarchical clustering results.

---

### 📌 Key Insights
- K-Means formed more granular groupings (4 clusters) while Hierarchical produced broader segmentation (2 clusters).
- Both methods yielded **similar silhouette scores**, suggesting good separation between clusters.
- K-Means had a higher Calinski–Harabasz score, indicating denser, well-separated clusters.

---
