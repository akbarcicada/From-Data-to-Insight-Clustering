# From-Data-to-Insight-Clustering

## Customer Segmentation with FMD using KMeans & DBSCAN

## 📌 Project Overview
This project explores **customer segmentation** using the **Online Retail 2010 dataset** (~30,000 rows).  
Segmentation is based on **FMD dimensions**:
- **Frequency** → how often a customer purchases (number of invoices)  
- **Monetary** → total transaction value (Quantity × Price)  
- **Diversity** → number of unique products purchased  

We applied **KMeans** and **DBSCAN** clustering algorithms, then compared their performance using **Silhouette Score** and **Davies-Bouldin Index**.

---

## 🛠️ Workflow
1. **Data Preprocessing**
   - Remove invalid transactions (Quantity ≤ 0, Price ≤ 0, StockCode contains "TEST")
   - Aggregate per customer into FMD features

2. **Feature Engineering**
   - Standardization with `StandardScaler`
   - Dimensionality reduction with PCA (2 components for visualization)

3. **KMeans Clustering**
   - Optimal `k` determined via **Elbow Method** and metrics
   - Final model used `k=3`

4. **DBSCAN Clustering**
   - Optimal parameters found with K-Distance Graph
   - Final model used `eps=0.7`, `min_samples=3`

5. **Evaluation**
   - Compare results of KMeans vs DBSCAN
   - Interpret customer segments (Low, Medium, Premium)

---

## 📊 Key Findings
- **KMeans (k=3)** identified:
  - Cluster 1: Low-value (largest group, minimal revenue contribution)
  - Cluster 2: Medium-value (bulk buyers, diverse products)
  - Cluster 3: Premium (VIP, wholesale/resellers, high contribution)

- **DBSCAN** identified:
  - One large low-value cluster
  - Two small medium-value clusters
  - Outlier segment = premium customers (highly valuable but rare)

---

## 🎯 Business Recommendations
- **Low Value Customers (majority)** → light promotions, upselling, cross-selling  
- **Medium Value Customers** → loyalty program, bundle offers, regular engagement  
- **Premium / VIP Customers (~3–4%)** → personalized service, exclusive discounts, account manager  

---

## 🚀 Tech Stack
- **Python** (pandas, numpy, scikit-learn)
- **Visualization**: matplotlib, seaborn
- **Clustering**: KMeans, DBSCAN
- **Dimensionality Reduction**: PCA

---

## 📌 Author
Ilham Akbar  
📧 [ilhamakr3301@gmail.com](mailto:ilhamakr3301@gmail.com)  
🔗 [LinkedIn](http://linkedin.com/in/ilham-akbar-3301abc)  
💻 [GitHub](https://github.com/akbarcicada)  


## 📂 Repository Structure
