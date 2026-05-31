# Financial Fraud Detection Using Explainable Machine Learning

This project focuses on building machine learning models capable of detecting fraudulent financial transactions under severe class imbalance.

The project explores how different machine learning models behave in fraud detection scenarios, with particular attention to recall, threshold tuning, explainability, and fraud pattern analysis.

Rather than treating fraud detection as only a classification problem, the project also considers some of the practical tradeoffs involved in real-world fraud systems such as false positives, customer friction, and missed fraud cases.

---

# Project Objectives

The main objective of this project is to build and compare multiple machine learning models for fraud detection using transactional financial data.

The project focuses on:

* fraud detection under highly imbalanced data
* transactional behavior analysis
* feature engineering
* model comparison across different model families
* threshold optimization
* explainability using SHAP
* fraud pattern interpretation

---

# Dataset

This project uses the PaySim Mobile Money Fraud Detection dataset from Kaggle.

The dataset contains simulated mobile money transactions with features related to:

* transaction type
* transaction amount
* sender and receiver balances
* account behavior
* fraud labels

The dataset is highly imbalanced, with fraudulent transactions representing only a very small fraction of total transactions.

---

# Machine Learning Workflow

## 1. Business Understanding, Data Audit & EDA

* business problem framing
* dataset overview
* class imbalance assessment
* transaction consistency investigation
* leakage assessment
* fraud behavior exploration
* transaction pattern analysis

---

## 2. Feature Engineering & Preprocessing

* behavioral feature engineering
* preprocessing pipeline
* categorical handling
* train-test splitting strategy
* imbalance handling techniques

---

## 3. Model Training & Comparison

### Baseline Model

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

## 4. Hyperparameter Tuning & Threshold Optimization

* hyperparameter tuning
* threshold engineering
* calibration analysis
* precision-recall tradeoff analysis

The project prioritizes fraud detection recall while still attempting to maintain manageable false positive rates.

---

## 5. SHAP Explainability & Insights

* global feature importance
* local prediction explanations
* fraud behavior interpretation
* model explainability analysis
* business insights and recommendations

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

# Current Status

Project currently in development.
