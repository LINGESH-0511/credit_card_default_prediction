# Credit Card Default Prediction

## Overview
This project predicts whether a customer will default on their credit card payment using machine learning.

It is a **binary classification problem** trained on real banking data.  
The goal is **risk detection**, not maximizing accuracy.

---

## Problem Statement
Credit card defaults cause financial losses to banks.  
By predicting default in advance, banks can take preventive actions such as:
- Reducing credit limits
- Flagging risky customers
- Improving risk management decisions

---

## Dataset
- Source: UCI Machine Learning Repository
- Name: Default of Credit Card Clients Dataset
- Records: 30,000
- Features: 23
- Target:
  - `1` → Default
  - `0` → No Default

Original target column name:



---

### Model Approach

- XGBoost Classifier is used as the primary model for predicting credit card default.
- Class imbalance is handled using the `scale_pos_weight` parameter to assign higher importance to the defaulter (minority) class.
- Since XGBoost is a tree-based model, feature scaling is not required.
- The model generates probability-based predictions, and a custom decision threshold is applied to improve recall for defaulters.


---

## Why Accuracy Is Not the Main Metric
In credit risk problems:
- Missing a defaulter (false negative) is costly
- Catching defaulters early is more important than overall accuracy

Therefore, **recall and ROC-AUC** are prioritized over accuracy.

---

## Model Evaluation Metrics
- Confusion Matrix
- Precision, Recall, F1-Score
- ROC-AUC Score

A lower accuracy with higher recall is **expected and acceptable**.

---

