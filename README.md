Medicare Provider Fraud Detection — Milestone 2

Machine Learning Project — GIU

Project Overview

This project focuses on detecting fraudulent Medicare providers using machine learning techniques.
The dataset contains:

Beneficiary demographic data

Outpatient and inpatient claims

Provider-level fraud labels (PotentialFraud)

The goal is to build a fully reproducible, end-to-end fraud detection system, including:

Data quality assessment

Exploratory Data Analysis (EDA)

Feature engineering at provider level

Handling severe class imbalance

Algorithm selection & model evaluation

Error analysis

Comprehensive documentation

This work corresponds to Milestone 2 of the Machine Learning Course project.

Team Members
Name	          ID	    
Youssef Wael	—	2003523
Omar Hefny	—	7002643
Ahmed Tamer	—	10002610
Jumana Hanafy - 13007113


Summary of Results

After extensive exploration and multiple modeling experiments, the following insights and conclusions were reached:

Best Performing Model: Logistic Regression

PR-AUC: 0.743 (Highest across all models)

Recall: 0.861 (Critical for fraud detection)

F1-score: 0.592

ROC-AUC: 0.952

Logistic Regression was chosen as the final model due to:

Strong performance on imbalanced metrics

Simplicity & interpretability

Auditability & transparency

Stable cross-validation performance

Consistent results with SMOTE + class weighting

Supporting Models
Model	PR-AUC	Notes
Random Forest	0.699	Strong precision, robust, less interpretable
Gradient Boosting	0.712	High recall, moderate precision
Decision Tree	0.520	Overfits easily, baseline only
SVM	0.474	Very high recall but poor precision
Error Analysis

False Positives (legitimate providers flagged): associated with

unusually high average reimbursement

abnormal inpatient ratios

heavy chronic-condition beneficiary mix

False Negatives (fraud not detected):

appear statistically “normal”

similar reimbursement patterns to legitimate providers

These insights guide future feature improvements.

Technologies & Libraries Used

Python 3.10+

Pandas — Data manipulation

NumPy — Numerical operations

Matplotlib & Seaborn — Visualization

Scikit-learn — Modeling & evaluation

Imbalanced-learn (SMOTE) — Class imbalance handling
