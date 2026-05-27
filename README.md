# Financial Fraud Detection Using Explainable Machine Learning

An end-to-end fraud detection project focused on explainability, imbalance learning, threshold optimization, and business-oriented machine learning.

This project explores how classical machine learning models can be used to identify fraudulent financial transactions while balancing fraud prevention, customer experience, and operational efficiency.

Rather than treating fraud detection as only a prediction problem, the project approaches it as a real-world decision system where model outputs directly affect customers, transaction flow, and fraud investigation processes.

---

# Project Objectives

The main goal of this project is to build and evaluate multiple machine learning models capable of detecting fraudulent transactions under severe class imbalance.

The project focuses on:

* fraud detection under imbalanced data
* feature engineering for transactional behavior
* model family comparison
* threshold optimization
* explainable AI using SHAP
* business-oriented evaluation
* fraud pattern analysis

---

# Dataset

This project uses the PaySim Mobile Money Fraud Detection dataset from [Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1?utm_source=chatgpt.com).

The dataset contains simulated mobile money transactions with features related to:

* transaction type
* account balances
* transfer amounts
* sender and receiver behavior


---

# Machine Learning Workflow

The project is organized into five main stages:

## 1. Business Understanding, Data Audit & EDA

* business problem framing
* dataset overview
* class imbalance analysis
* leakage investigation
* fraud behavior exploration
* transaction pattern analysis

---

## 2. Feature Engineering & Preprocessing

* behavioral feature engineering
* encoding and transformations
* imbalance handling
* train-test strategy
* preprocessing pipeline

---

## 3. Model Training & Comparison

### Naive Baseline

* DummyClassifier

### Linear & Probabilistic Models

* Logistic Regression
* SGDClassifier
* Gaussian Naive Bayes

### Tree-Based Models

* Decision Tree
* Random Forest

### Boosted Ensemble Models

* AdaBoost
* Gradient Boosting
* XGBoost
* LightGBM
* CatBoost

Models will be evaluated using:

* Recall
* Precision
* F1-score
* ROC-AUC
* PR-AUC

---

## 4. Hyperparameter Tuning & Threshold Engineering

* hyperparameter optimization
* threshold tuning
* calibration analysis
* precision-recall tradeoff analysis

The project prioritizes fraud detection recall while maintaining operationally manageable false positive rates.

---

## 5. SHAP Explainability & Business Insights

* global feature importance
* local prediction explanations
* fraud behavior interpretation
* business recommendations
* model governance discussion

---

# Project Structure

```text
fraud-detection-ml/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_business_understanding_data_audit_eda.ipynb
│   ├── 02_feature_engineering_preprocessing.ipynb
│   ├── 03_model_training_comparison.ipynb
│   ├── 04_hyperparameter_threshold_optimization.ipynb
│   └── 05_shap_insights_recommendations.ipynb
│
├── visuals/
├── models/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* LightGBM
* CatBoost
* SHAP
* imbalanced-learn

---

# Key Focus Areas

This project emphasizes:

* explainable machine learning
* fraud intelligence analysis
* business-aware model evaluation
* threshold optimization
* operational tradeoffs
* realistic fraud detection challenges

---

# Status

Project currently in development.
