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

## Approach
- Logistic Regression (baseline model)
- Feature scaling using StandardScaler
- Class imbalance handled using `class_weight="balanced"`
- Custom decision threshold to improve recall

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

## Project Structure
