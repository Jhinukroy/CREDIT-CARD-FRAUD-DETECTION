# Credit Card Fraud Detection using Advanced Ensemble Learning

This project builds a highly optimized machine learning pipeline to detect fraudulent credit card transactions using the Kartik Shenoy Kaggle dataset. Because fraud datasets are heavily imbalanced, this project evaluates multiple linear and tree-based models, focusing heavily on the trade-off between predictive accuracy and computational training speed.

## 🚀 Model Performance Summary

While multiple algorithms achieved high baseline performance, **Gradient Boosting and XGBoost** emerged as the top contenders for deployment.

| Model | Test Accuracy | Computational Efficiency / Notes |
| :--- | :--- | :--- |
| **Gradient Boosting** | **0.9952** | **Highest performance; preferred choice for deployment.** |
| **XGBoost** | **0.9951** | Identical performance to Gradient Boosting, but trains faster on large scales. |
| **Random Forest** | 0.9948 | Strong performance, but takes significantly longer to train on large datasets. |
| **Logistic Regression** | 0.9947 | Excellent, fast linear baseline. |
| **Decision Tree** | 0.9929 | Fast but prone to minor overfitting. |
| **Linear Discriminant Analysis (LDA)**| 0.9911 | Solid baseline for pure linear classification. |

> **Key Engineering Insight:** Although Random Forest performs competitively, it becomes a massive computational bottleneck on large data scales. Gradient Boosting (and its optimized counterpart XGBoost) is preferred for large-scale credit card data due to superior scaling and optimization capabilities.

---

## 🛠️ Features & Methodology

*   **Imbalance Handling:** Evaluated using strict stratify-splits to ensure minority fraud classes are equally represented in training and testing phases.
*   **Feature Engineering:** Standard Scaling applied to transaction amounts (`amt`) and Unix timestamps to normalize features for linear baselines like Logistic Regression and LDA.
*   **Scalability Analysis:** Monitored and documented training time trade-offs between Parallel Random Forests vs. Sequential Tree Boosting.

---

## 📦 Getting Started

### Prerequisites
Make sure you have Python 3.8+ installed.

### Get the Data:

Download the dataset from Kaggle.

Place fraudTrain.csv and fraudTest.csv inside the data/ directory.

https://www.kaggle.com/datasets/kartik2112/fraud-detection



