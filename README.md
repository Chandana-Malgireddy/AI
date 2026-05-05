# Credit Card Fraud Detection using Autoencoder, XGBoost, and Agentic LLM

## Overview

This project presents a hybrid AI-based credit card fraud detection system that combines anomaly detection, supervised machine learning, and LLM-based reasoning. The goal is to detect fraudulent transactions accurately while also providing explainable investigation-style reasoning for flagged cases.

The system uses a three-stage pipeline:

1. **Autoencoder** for anomaly detection  
2. **XGBoost** for supervised fraud classification  
3. **Agentic LLM** for transaction-level reasoning and explanation  

This approach improves both fraud detection performance and interpretability.

---

## Problem Statement

Credit card fraud detection is challenging because fraudulent transactions are rare, patterns change over time, and false positives can affect genuine customers. Traditional machine learning models can classify fraud, but they often provide limited reasoning behind predictions.

This project addresses the problem by combining deep anomaly detection, supervised classification, and LLM-based explanation to support more reliable and interpretable fraud detection.

---

## Dataset

The project uses the Kaggle Credit Card Transactions Fraud Detection dataset.

Dataset files:

- `fraudTrain.csv`
- `fraudTest.csv`

Combined dataset size:

- Training records: 1,296,675
- Testing records: 555,719
- Total records: 1,852,394

The dataset contains transaction details such as transaction amount, merchant, category, customer demographics, location, timestamp, and fraud label.

Dataset link:

https://www.kaggle.com/datasets/kartik2112/fraud-detection

---

## Key Features

- End-to-end fraud detection pipeline
- Severe class imbalance handling
- Feature engineering using transaction behavior, time, location, and amount patterns
- Autoencoder-based reconstruction error as anomaly signal
- XGBoost classifier for final fraud prediction
- LLM-based reasoning for explainable fraud investigation
- Evaluation using recall, precision, F1-score, PR-AUC, and confusion matrix

---

## System Architecture

```text
Raw Transaction Data
        |
        v
Data Preprocessing
        |
        v
Feature Engineering
        |
        v
Autoencoder Model
        |
        v
Reconstruction Error Feature
        |
        v
XGBoost Classifier
        |
        v
Fraud / Non-Fraud Prediction
        |
        v
Agentic LLM Reasoning
        |
        v
Explainable Fraud Decision
