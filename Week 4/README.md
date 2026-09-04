# Predictive Analytics Model Plan — Customer Churn Prediction (Week 4)

 **A staged, evidence-based strategy for building a customer churn prediction model using the UCI Online Retail Dataset.**

---

##  Executive Summary

This repository outlines the complete predictive modeling plan for **Week 4** of the advanced predictive analytics project. The objective is to design, evaluate, and operationalize a machine learning pipeline to identify customers at risk of churn. By progressing from interpretable linear baselines to complex ensemble techniques, the project balances model explainability with high predictive performance.

---

##  Table of Contents

* **Overview & Goals**
* **Project Pipeline & Methodology**
* **Model Selection Strategy**
* **Evaluation Metrics & Validation**
* **Key Dataset Insights**
* **Limitations & Mitigation Strategies**

---

##  Overview & Goals

* **Problem Statement:** Customer churn directly impacts long-term customer lifetime value (CLV). Identifying high-risk churners early enables targeted retention strategies.
* **Core Goal:** Transition from exploratory data analysis (EDA) to a robust modeling strategy using stratified splitting and cross-validation to select production-ready models.
* **Key Metric Target:** Prioritize **Recall** and **F1-Score** over raw accuracy due to class imbalance and the higher business cost of false negatives (missing an actual churner).

---

##  Project Pipeline & Methodology

```text
[ Raw UCI Retail Data ] ➡️ [ Data Preprocessing & Cleaning ] ➡️ [ Feature Engineering & Selection ]
                                                                             │
[ Model Deployment & Retention Strategies ] ⬅️ [ Evaluation (Recall/F1) ] ⬅️ [ Model Comparison & Tuning ]

```

1. **Preprocessing & Data Hygiene:** Address missing customer identifiers, remove negative quantity anomalies (returns/cancellations), and handle extreme price outliers.
2. **Feature Engineering:** Calculate Recency, Frequency, and Monetary (RFM) metrics along with product-demand concentration features.
3. **Validation Strategy:** Implement stratified Train/Validation/Test splits alongside $k$-fold cross-validation to eliminate data leakage and prevent overfitting.

---

##  Model Selection Strategy

| Model Stage | Algorithm | Primary Purpose | Key Advantages |
| --- | --- | --- | --- |
| **Baseline** | **Logistic Regression** | Interpretable Benchmark | Highly transparent, fast baseline performance metrics |
| **Intermediate** | **Decision Trees** | Non-Linearity Probing | Uncovers non-linear decision boundaries and interaction terms |
| **Production Candidates** | **Random Forest & Gradient Boosting** | High-Accuracy Deployment | Superior predictive power, handles non-linear relationships, robust against noise |

---

##  Evaluation Metrics

Because identifying churners is critical, evaluation relies on metrics tailored for imbalanced classification:

* **Recall:** Minimizes missed churners (False Negatives).
* **F1-Score:** Balances Precision and Recall to ensure retention budgets aren't wasted on False Positives.
* **Precision & ROC-AUC:** Used as secondary check metrics during cross-validation tuning.

---

##  Limitations & Mitigation Strategies

* **Class Imbalance:** Handled via SMOTE/undersampling techniques and threshold adjustment.
* **Data Quality Issues:** Filtered extreme price outliers and omitted missing customer IDs while retaining transaction integrity.
* **Concept Drift:** Planned periodic model monitoring and regular retraining schedules post-deployment.

---

