#  Telco Customer Churn Prediction & Customer Segmentation Pipeline

#  Project Overview

This repository contains an **End-to-End Machine Learning Pipeline** developed using a real-world **Telecom Customer Dataset**. The primary goal is twofold:

1. **Supervised Learning:** Predict customer churn (whether a customer will leave the service) to enable proactive retention strategies.

2. **Unsupervised Learning:** Group customers into distinct behavioral segments to help marketing teams tailor personalized offers.



# Project Architecture & Workflow

text
Raw Telecom Data 
Data Cleaning & Preprocessing 
 Exploratory Data Analysis (EDA)
 Model Training 
 Clustering 
 Business Insights

1. Data Preparation & Preprocessing

-Missing Value Imputation: Handled blank/missing numerical entries (e.g., TotalCharges).
-Categorical Encoding: Applied One-Hot Encoding and Label Encoding to transform non-numeric attributes into machine-readable format.
-Feature Scaling: Scaled numeric features using StandardScaler (essential for distance-based models like SVM and K-Means).

2. Exploratory Data Analysis (EDA) & Visualization
-Visualized key retention metrics, monthly charge distributions, and tenure trends.
-Analyzed feature correlation matrices to identify strong churn drivers (e.g., contract type, payment methods).

# Machine Learning Modeling
- Supervised Learning (Churn Classification)
Trained, tuned, and evaluated 5 distinct algorithms across tree-based, linear, and ensemble paradigms:
-Decision Tree Classifier
-Support Vector Machine (SVM)
-Random Forest Classifier
-Bagging Classifier
-Boosting (AdaBoost / XGBoost / GradientBoosting)

# Unsupervised Learning (Customer Segmentation)
Identified hidden customer sub-groups based on tenure, monthly spending, and service usage:

-K-Means Clustering: Determined optimal cluster count ($K$) using the Elbow Method and Silhouette Analysis.
-Agglomerative Hierarchical Clustering: Built hierarchical structure and visualized cluster relationships using Dendrograms.

# Evaluation Strategy & Performance Metrics
To account for class imbalance inherent in customer churn datasets, models were comprehensively benchmarked using:
-Classification Metrics: Accuracy, Precision, Recall, Macro F1-Score, Weighted F1-Score, and Confusion Matrix.
-Clustering Metrics: Silhouette Score, Davies-Bouldin Index.

# Key Benchmark Note: Recall and Macro F1-Score were prioritized to minimize False Negatives (unidentified churning customers).


---

# Repository Structure

`text
├── Telco_Customer_Churn_Analysis.ipynb  # Primary Google Colab Notebook

├── requirements.txt                      # Required Dependencies & Libraries

└── README.md                            # Project Documentation


#How to Run
Open the notebook in Google Colab.

Install the packages listed in requirements.txt if needed.

Run the notebook cells from top to bottom.

Review the model comparison and final insights.
