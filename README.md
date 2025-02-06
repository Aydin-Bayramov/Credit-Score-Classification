# Credit Score Analysis and Classification

This repository contains a comprehensive workflow for analyzing and classifying customer credit scores using machine learning techniques. Below is an overview of the project, tools used, and the methodology implemented.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Dataset Overview](#dataset-overview)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Data Preprocessing](#data-preprocessing)
6. [Model Training and Evaluation](#model-training-and-evaluation)
7. [Results](#results)
8. [License](#license)

---

## Introduction
This project focuses on predicting customer credit scores (categorized as `Good`, `Standard`, or `Poor`) based on financial and behavioral data. By leveraging data exploration, feature engineering, and machine learning, we aim to achieve high prediction accuracy while gaining insights into the key factors affecting credit scores.

---

## Installation
To set up the environment and run the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Place the dataset (`train.csv`) in the project root directory.

---

## Dataset Overview
The dataset contains 100,000 entries with 28 columns describing customers' financial and credit history. Key columns include:

| Variable Name           | Description                                             |
|-------------------------|---------------------------------------------------------|
| `Age`                  | Customer's age                                         |
| `Annual_Income`        | Annual income                                          |
| `Credit_Score`         | Target variable (Good, Standard, Poor)                 |
| `Num_Bank_Accounts`    | Number of bank accounts                                |
| `Outstanding_Debt`     | Remaining debt                                         |
| `Payment_Behaviour`    | Payment behavior (e.g., Low/High spent)               |

---

## Exploratory Data Analysis (EDA)
We performed EDA to identify patterns and visualize key relationships:

1. **Credit Score Distribution**: A count plot to understand the distribution of credit scores.
2. **Income vs. Credit Score**: A boxplot to analyze the impact of annual income on credit scores.
3. **Credit Mix Analysis**: Count plots segmented by `Credit Mix` and `Credit Score`.
4. **Age of Credit History**: Visualized using boxplots segmented by credit score categories.

### Example Visualization:
![Credit Score Distribution](images/credit_score_distribution.png)

---

## Data Preprocessing
1. Dropped irrelevant columns (`ID`, `Customer_ID`, `Name`, `SSN`).
2. Transformed `Type_of_Loan` into binary indicators for top loan categories.
3. Encoded categorical features (`Occupation`, `Payment_Behaviour`, etc.) using `OrdinalEncoder`.
4. Separated features (`X`) and target variable (`y`).
5. Split the data into training (80%) and testing (20%) sets.

---

## Model Training and Evaluation
We used a `RandomForestClassifier` to predict credit scores, with hyperparameter tuning performed using `RandomizedSearchCV` and `StratifiedKFold` cross-validation. The best hyperparameters were:

- `n_estimators`: 300
- `max_depth`: 20
- `min_samples_split`: 10
- `min_samples_leaf`: 5

### Evaluation Metrics
Performance was evaluated using precision, recall, F1-score, and accuracy for both training and testing sets.

#### Training Set Results:
| Metric      | Precision | Recall | F1-Score | Accuracy |
|-------------|-----------|--------|----------|----------|
| `Good`      | 0.83      | 0.86   | 0.84     | 87%      |
| `Standard`  | 0.86      | 0.87   | 0.87     |          |
| `Poor`      | 0.89      | 0.88   | 0.89     |          |

#### Testing Set Results:
| Metric      | Precision | Recall | F1-Score | Accuracy |
|-------------|-----------|--------|----------|----------|
| `Good`      | 0.73      | 0.78   | 0.75     | 80%      |
| `Standard`  | 0.79      | 0.80   | 0.79     |          |
| `Poor`      | 0.83      | 0.81   | 0.82     |          |

---

## Results
The Random Forest model achieved an overall accuracy of 80% on the test set, with strong performance in distinguishing between `Good`, `Standard`, and `Poor` credit scores. Feature importance analysis highlighted key factors like `Annual_Income`, `Credit_History_Age`, and `Outstanding_Debt`.
