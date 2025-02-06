# Credit Score Analysis and Classification

Welcome to the **Credit Score Analysis and Classification** repository! This project leverages machine learning techniques to analyze and classify customer credit scores, providing insights into financial behavior and predictive analytics.

---

## 🚀 Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Dataset Overview](#dataset-overview)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Model Training and Evaluation](#model-training-and-evaluation)
6. [Results](#results)
---

## 🌟 Introduction

Credit scoring plays a critical role in financial decision-making, impacting loans, credit card approvals, and more. This project aims to:

- Predict credit scores (`Good`, `Standard`, or `Poor`) using machine learning models.
- Understand key factors influencing credit scores through data analysis and feature importance.
- Provide a reproducible pipeline for future credit score projects.

---

## ✨ Features

- **Data Preprocessing**: Handles missing values, feature encoding, and scaling.
- **EDA and Visualizations**: Gain insights through descriptive statistics and plots.
- **Machine Learning Models**: Implements `RandomForestClassifier` with hyperparameter tuning.
- **Reproducibility**: Modular codebase with detailed instructions.

---

## 📊 Dataset Overview

The dataset comprises **100,000 entries** with **28 features**, including financial and behavioral attributes. Below are some key columns:

| Variable Name         | Description                                   |
|-----------------------|-----------------------------------------------|
| `Age`                | Customer's age                               |
| `Annual_Income`      | Annual income in USD                        |
| `Credit_Score`       | Target variable (`Good`, `Standard`, `Poor`) |
| `Num_Bank_Accounts`  | Total number of bank accounts               |
| `Outstanding_Debt`   | Total outstanding debt                      |
| `Payment_Behaviour`  | Payment patterns (e.g., `High Spent`)       |

---

## 🔍 Exploratory Data Analysis (EDA)

EDA highlights patterns and relationships in the data. Key visualizations include:

- **Credit Score Distribution**: Understand the balance across score categories.
- **Income vs. Credit Score**: Analyze the impact of annual income on scores.
- **Credit History Analysis**: Examine the role of credit history length.

---

## 🧪 Model Training and Evaluation

### Model: Random Forest Classifier

Key steps include:

1. **Hyperparameter Tuning**: Performed using `RandomizedSearchCV`.
2. **Cross-Validation**: Ensures robust performance metrics.

#### Best Hyperparameters
- `n_estimators`: 300
- `max_depth`: 20
- `min_samples_split`: 10
- `min_samples_leaf`: 5

#### Evaluation Metrics

| Metric      | Training Precision | Testing Precision |
|-------------|---------------------|--------------------|
| `Good`      | 0.83               | 0.73              |
| `Standard`  | 0.86               | 0.79              |
| `Poor`      | 0.89               | 0.83              |

Overall Test Accuracy: **80%**

---

## 🎯 Results

- **Key Factors**: `Annual_Income`, `Credit_History_Age`, and `Outstanding_Debt` emerged as the most influential features.
- **Model Performance**: The model achieves reliable classification across all credit score categories, suitable for real-world applications.

