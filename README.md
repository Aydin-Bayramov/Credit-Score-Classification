# Credit Score Analysis and Classification

Welcome to the **Credit Score Analysis and Classification** repository! This project leverages machine learning techniques to analyze and classify customer credit scores, providing insights into financial behavior and predictive analytics.

---

## 🚀 Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Dataset Overview](#dataset-overview)
6. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
7. [Model Training and Evaluation](#model-training-and-evaluation)
8. [Results](#results)
9. [Contributing](#contributing)
10. [License](#license)

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

## 🛠️ Installation

Follow these steps to set up the project locally:

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Add the dataset (`train.csv`) to the project root directory.

---

## 📖 Usage

1. Preprocess the data:
   ```bash
   python preprocess.py
   ```
2. Perform exploratory data analysis:
   ```bash
   python eda.py
   ```
3. Train the model:
   ```bash
   python train.py
   ```
4. Evaluate the results:
   ```bash
   python evaluate.py
   ```

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

Example:
![Credit Score Distribution](images/credit_score_distribution.png)

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

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit changes and push:
   ```bash
   git push origin feature-branch
   ```
4. Submit a pull request for review.

---

## 📜 License

This project is licensed under the **MIT License**. Feel free to use, modify, and distribute the code with attribution.

---

Happy Coding! 💻✨

