# 👥 Telecom Customer Segmentation Engine

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-red?logo=scikit-learn)](https://scikit-learn.org/)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen)]()

## 📌 Business Overview
In the highly competitive telecommunications sector, retaining a customer is significantly more cost-effective than acquiring a new one. The goal of this project is to build an **unsupervised machine learning pipeline** that segments customers based on usage behaviors, allowing business stakeholders to identify high-risk churn profiles without relying on explicit historical labels.

## ⚙️ Technical Approach
This project utilizes **K-Means Clustering** coupled with **Principal Component Analysis (PCA)** for dimensionality reduction. 
* **Optimal K Selection:** Leveraged the Elbow Method and Silhouette Score to determine the optimal number of clusters (K=2).
* **Dimensionality Reduction:** Applied PCA to reduce the feature space to 2 dimensions, explaining ~20% of the variance for visual interpretation of cluster boundaries.
* **Feature Scaling:** Standardized 11 continuous features (call minutes, international usage, customer service calls) using `StandardScaler` to ensure distance-based metrics functioned correctly.

## 📊 Key Findings & Business Impact
By profiling the resulting clusters, the model successfully isolated distinct behavioral groups:
* **High-Risk Segment Isolated:** The model identified a specific cluster of customers (characterized by zero voicemail plan usage and high customer service calls) that exhibited a churn rate of **17%**, compared to the secondary cluster's **9%**.
* **Actionable Insight:** Marketing and retention teams can use this segmentation to proactively target the high-risk cluster with targeted promotions (e.g., discounted voicemail plans) before they churn.

## 🧰 Tech Stack
* **Language:** Python
* **Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

## 🚀 How to Run Locally
1. Clone this repository.
2. Ensure you have the required libraries installed (`pip install -r requirements.txt` or install manually).
3. Run the Jupyter Notebook `customer_segmentation_kmeans.ipynb` to view the analysis and visualizations.
