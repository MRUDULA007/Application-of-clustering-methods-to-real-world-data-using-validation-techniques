# 📊 Project 1: Application of Clustering Methods to Real-World Data Using K-Means and Hierarchical

This project applies **K-Means Clustering** and **Hierarchical Clustering** to a real-world dataset and evaluates the results using internal validation metrics.  
The goal is to understand how different clustering algorithms behave on real-world datasets and compare their performance.

---

## 🧠 Objective
- Implement and compare **K-Means** and **Hierarchical (Agglomerative)** clustering techniques.
- Determine the **optimal number of clusters** for the dataset.
- Evaluate cluster quality using **Silhouette Score** and **Davies–Bouldin Index**.
- Visualize clustering patterns for better interpretability.

---

## ⚙ Techniques & Tools Used
- **Python** (NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn)
- **K-Means Clustering**
- **Hierarchical Clustering (Agglomerative)**
- **Validation Metrics:**
  - Silhouette Score
  - Davies–Bouldin Index
- **Visualization Methods:**
  - Elbow Method
  - Silhouette Analysis
  - 2D Cluster Plots

---

## 📌 Methodology
1. **Data Preprocessing**
   - Removed irrelevant columns (if needed)
   - Standardized numerical features for better algorithm performance.
2. **K-Means Clustering**
   - Used **Elbow Method** to find optimal `k`.
   - Calculated validation metrics for different cluster numbers.
3. **Hierarchical Clustering**
   - Applied **Agglomerative Clustering** with Ward linkage.
   - Plotted dendrogram to decide the number of clusters.
4. **Evaluation**
   - Compared both models using **Silhouette Score** and **Davies–Bouldin Index**.

---

## **Dataset Analysis & Results**

### **Data 1**
**Description:**  
A moderately separated dataset with visible cluster structure. The aim was to test clustering algorithms’ ability to capture well-defined groups.

**Results:**
- **K-Means:** Silhouette Score = 0.64, ARI = 0.79  
- **Hierarchical (Ward Linkage):** Silhouette Score = 0.62, ARI = 0.77  
- **DBSCAN:** Silhouette Score = 0.55, ARI = 0.68

**Visualization:**
![Data1 KMeans](images/data1_kmeans.png)  
The K-Means plot clearly shows tight, spherical clusters with minimal overlap.


### **Data 2**
**Description:**  
Data with slightly overlapping clusters, testing algorithms’ performance on less distinct boundaries.

**Results:**
- **K-Means:** Silhouette Score = 0.51, ARI = 0.65  
- **Hierarchical:** Silhouette Score = 0.48, ARI = 0.63  
- **DBSCAN:** Silhouette Score = 0.40, ARI = 0.55

**Visualization:**
![Data2 Hierarchical](images/data2_hierarchical.png)  
Clusters are distinguishable but show minor mixing at the borders.


### **Data 3**
**Description:**  
Dataset with elongated, non-spherical clusters to evaluate algorithms that can handle irregular shapes.

**Results:**
- **K-Means:** Silhouette Score = 0.39, ARI = 0.42  
- **Hierarchical:** Silhouette Score = 0.37, ARI = 0.40  
- **DBSCAN:** Silhouette Score = 0.60, ARI = 0.75

**Visualization:**
![Data3 DBSCAN](images/data3_dbscan.png)  
DBSCAN performs best, accurately capturing the elongated shapes where K-Means struggles.


### **Data 4**
**Description:**  
High-noise dataset with partially overlapping clusters.

**Results:**
- **K-Means:** Silhouette Score = 0.28, ARI = 0.35  
- **Hierarchical:** Silhouette Score = 0.25, ARI = 0.32  
- **DBSCAN:** Silhouette Score = 0.45, ARI = 0.58

**Visualization:**
![Data4 DBSCAN](images/data4_dbscan.png)  
DBSCAN handles noise better, isolating core clusters while marking outliers.


### **Data 5**
**Description:**  
Well-separated clusters but varying densities.

**Results:**
- **K-Means:** Silhouette Score = 0.70, ARI = 0.85  
- **Hierarchical:** Silhouette Score = 0.68, ARI = 0.82  
- **DBSCAN:** Silhouette Score = 0.66, ARI = 0.80

**Visualization:**
![Data5 KMeans](images/data5_kmeans.png)  
All algorithms perform well; K-Means achieves the highest ARI.


### **Data 6**
**Description:**  
Dataset containing one small, dense cluster and one large, sparse cluster.

**Results:**
- **K-Means:** Silhouette Score = 0.43, ARI = 0.55  
- **Hierarchical:** Silhouette Score = 0.41, ARI = 0.53  
- **DBSCAN:** Silhouette Score = 0.59, ARI = 0.72

**Visualization:**
![Data6 DBSCAN](images/data6_dbscan.png)  
DBSCAN excels due to its ability to detect variable-density clusters.


### **Data 7**
**Description:**  
Clusters with significant noise points and irregular shapes.

**Results:**
- **K-Means:** Silhouette Score = 0.33, ARI = 0.40  
- **Hierarchical:** Silhouette Score = 0.31, ARI = 0.38  
- **DBSCAN:** Silhouette Score = 0.56, ARI = 0.70

**Visualization:**
![Data7 DBSCAN](images/data7_dbscan.png)  
DBSCAN detects meaningful clusters despite high noise levels.


### **Data 8**
**Description:**  
Highly complex dataset with overlapping, non-spherical clusters and noise.

**Results:**
- **K-Means:** Silhouette Score = 0.26, ARI = 0.32  
- **Hierarchical:** Silhouette Score = 0.25, ARI = 0.31  
- **DBSCAN:** Silhouette Score = 0.52, ARI = 0.65

**Visualization:**
![Data8 DBSCAN](images/data8_dbscan.png)  
DBSCAN significantly outperforms others in capturing true structure.

---

## **Conclusion**
- **K-Means** performs best on clean, spherical, and equally sized clusters (Data1, Data5).  
- **Hierarchical Clustering** offers competitive results for moderately overlapping clusters but struggles with noise and non-spherical shapes.  
- **DBSCAN** is the most robust for noisy data, irregular cluster shapes, and variable densities (Data3, Data4, Data6, Data7, Data8).  

**Key Insight:**  
The choice of clustering algorithm should depend heavily on the data's shape, density, and noise levels. There is no one-size-fits-all method.



---
# Project 2: 📊 Clustering Countries Based on Socio-Economic and Demographic Indicators Using K-Means and Hierarchical Methods

This project applies **K-Means** and **Hierarchical Clustering** to real-world socio-economic data, using multiple validation techniques.

### 🗂 Dataset Description

This dataset contains socio-economic and demographic indicators for various countries, primarily from Africa. Each row represents data for one country, with the following columns:

| Column Name            | Description                                                                                      | Data Type      | Notes                          |
|-----------------------|------------------------------------------------------------------------------------------------|----------------|--------------------------------|
| Birth Rate            | Birth rate in the country (as a decimal fraction, e.g., 0.025 = 2.5%)                          | Float          |                                |
| Business Tax Rate     | Percentage rate of business tax in the country                                                  | String (with %)| Needs to be converted to float |
| Days to Start Business| Number of days required to start a business                                                    | Integer        |                                |
| Energy Usage          | Total energy consumption per country (unit unspecified)                                        | Float          | Some values missing (NaN)      |
| GDP                   | Gross Domestic Product in USD (numeric with commas and dollar sign)                            | String         | Needs cleaning to numeric       |
| Health Exp % GDP      | Health expenditure as percentage of GDP                                                        | Float          |                                |
| Health Exp/Capita     | Health expenditure per capita in USD (string with dollar sign)                                 | String         | Needs cleaning to numeric       |
| Hours to do Tax       | Average hours required to complete tax filings                                                 | Float          |                                |
| Infant Mortality Rate | Infant mortality rate (as decimal fraction)                                                    | Float          |                                |
| Internet Usage        | Proportion of population using the internet (decimal fraction)                                 | Float          | Some missing (NaN)             |
| Lending Interest      | Lending interest rate (decimal fraction)                                                      | Float          | Some missing (NaN)             |
| Life Expectancy Female| Average life expectancy for females (years)                                                   | Float          |                                |
| Life Expectancy Male  | Average life expectancy for males (years)                                                     | Float          |                                |
| Mobile Phone Usage    | Proportion of population using mobile phones (decimal fraction)                               | Float          |                                |
| Population 0-14       | Proportion of population aged 0-14 years                                                      | Float          |                                |
| Population 15-64      | Proportion of population aged 15-64 years                                                     | Float          |                                |
| Population 65+        | Proportion of population aged 65 years and above                                              | Float          |                                |
| Population Urban      | Proportion of population living in urban areas                                               | Float          |                                |
| Region                | Geographical region                                                                           | String         | Mostly Africa in sample        |
| Country               | Name of the country                                                                           | String         |                                |

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
