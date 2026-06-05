# Financial Fraud Detection Using Explainable Machine Learning

This project focuses on building machine learning models capable of detecting fraudulent financial transactions in highly imbalanced financial datasets.

The project explores how different machine learning models behave in fraud detection scenarios, with particular attention to recall optimization, threshold tuning, explainability, and fraud behavior analysis.

Rather than treating fraud detection as only a classification problem, the project also considers practical real-world tradeoffs such as false positives, customer friction, operational fraud monitoring, and missed fraud cases.

---

# Project Objectives

The main objective of this project is to build and compare multiple machine learning models for detecting fraudulent financial transactions using transactional behavioral data.

The project focuses on:

* fraud detection under severe class imbalance
* transactional behavior analysis
* feature engineering
* model comparison across different model families
* hyperparameter tuning
* threshold optimization
* explainability using SHAP
* fraud pattern interpretation
* business insights and operational recommendations

---

# Dataset

This project uses the PaySim Mobile Money Fraud Detection dataset from Kaggle.

The dataset contains simulated mobile money transactions with features related to:

* transaction type
* transaction amount
* sender and receiver balances
* account balance transitions
* transactional behavior patterns
* fraud labels

The dataset is highly imbalanced, with fraudulent transactions representing only a very small percentage of total transactions.

During experimentation, suspiciously high evaluation metrics were initially observed after introducing engineered balance error features. Further investigation suggested that these variables artificially simplified fraud separability and inflated model performance. To maintain a more realistic fraud detection pipeline, the balance error features were removed from the final modeling workflow.

---

# Machine Learning Workflow

## 1. Business Understanding, Data Audit & EDA

* business problem framing
* dataset overview
* class imbalance assessment
* transaction consistency investigation
* fraud behavior exploration
* transaction pattern analysis
* suspicious feature investigation

---

## 2. Feature Engineering & Preprocessing

* behavioral feature engineering
* preprocessing pipeline
* categorical feature encoding
* train-test splitting strategy
* imbalance handling techniques
* feature selection and leakage control

---

## 3. Model Training & Comparison

### Baseline Model

* DummyClassifier

### Linear & Probabilistic Models

* Logistic Regression
* SGDClassifier
* Gaussian Naive Bayes

### Distance-Based Models

* K-Nearest Neighbors (KNN)


### Tree-Based Models

* Decision Tree
* Random Forest

### Boosted Ensemble Models

* AdaBoost
* Gradient Boosting
* XGBoost
* LightGBM
* CatBoost

Models were evaluated using:

* Recall
* Precision
* F1-score
* ROC-AUC

---

## 4. Hyperparameter Tuning & Threshold Optimization

* randomized hyperparameter tuning
* precision-recall tradeoff analysis
* threshold optimization
* confusion matrix evaluation
* operational fraud tradeoff analysis

The project prioritizes fraud detection recall while still maintaining manageable false positive rates for practical fraud monitoring scenarios.

After optimization and evaluation, XGBoost was selected as the final fraud detection model based on its strong recall performance, balanced precision, and overall operational fraud detection capability.

---

## 5. SHAP Explainability & Business Insights

* SHAP summary analysis
* fraud-driving feature interpretation
* transaction behavior analysis
* explainable fraud prediction analysis
* business insights and operational recommendations

The explainability phase focused on understanding how transaction patterns, account balance behavior, and transaction types influenced fraud predictions within the final XGBoost model.

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

# Final Outcome

The project successfully developed an explainable machine learning fraud detection pipeline capable of identifying fraudulent financial transactions under severe class imbalance.

The final XGBoost model achieved strong fraud detection performance while balancing fraud sensitivity and false positive control. SHAP analysis further helped explain how transaction patterns and account behavior influenced fraud predictions, improving model transparency and business interpretability.

The project demonstrates how machine learning can support operational fraud monitoring systems through behavioral transaction analysis, threshold optimization, and explainable fraud prediction workflows.
