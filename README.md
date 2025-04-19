# 📉 Customer Churn Prediction

This project builds a machine learning pipeline to predict **customer churn** using a bank customer dataset. Churn refers to whether a customer leaves the bank (Exited = 1) or not (Exited = 0). The pipeline includes data preprocessing, exploratory analysis, feature engineering, and model training using **CatBoost** and **Random Forest** classifiers.

---

## 📌 Project Overview

The goal is to predict whether a customer will churn based on demographic and financial attributes. The final model outputs a probability score for each customer, and results are submitted as a CSV for evaluation.

---

## ✅ Objectives

- Explore the distribution of key features such as **Geography**, **Gender**, and **Churn status**.
- Analyze correlations between numeric features and churn.
- Visualize churn behavior by **country**, **gender**, and **key numeric factors**.
- Apply preprocessing using **OneHotEncoding** and **StandardScaler**.
- Train robust classifiers to predict churn probability.
- Evaluate models using **AUC Score**.

---

## 📊 Data Description

- `train.csv`: Main training dataset
- `test.csv`: Unlabeled test dataset
- `submission.csv`: Template for submission format

**Dropped Columns**:
- `id`, `CustomerId`, and `Surname` were dropped as they are identifiers or irrelevant to prediction.

---

## 🔍 Exploratory Data Analysis

### 📦 Categorical Feature Distributions
- Bar plots of `Geography`, `Gender`, and `Exited`

### 📈 Correlation Heatmap
- Shows relationships between numeric features such as `CreditScore`, `Age`, `Balance`, etc.

### 📊 Churn Analysis by Groups
- Bar charts comparing churn rate by:
  - **Geography**
  - **Gender**

### 📉 Box Plots of Key Features by Churn Status
- Features analyzed: `CreditScore`, `Age`, `Tenure`, `Balance`, `NumOfProducts`, `EstimatedSalary`

---

## ⚙️ Feature Engineering

- **Categorical features**: `Geography`, `Gender`
- **Numerical features**: All other predictors
- **Preprocessing pipeline**:
  - Standard scaling of numeric data
  - One-hot encoding of categorical variables (dropping first category)

---

## 🧪 Model Training & Evaluation

### ✅ 1. CatBoost Classifier
- Parameters: `depth=4`, `iterations=1000`, `learning_rate=0.01`, `l2_leaf_reg=5`
- Trained using pipeline with preprocessing
- **Evaluation Metric**: ROC AUC Score

### ✅ 2. Random Forest Classifier
- Included as a second model for comparison
- Trained using the same pipeline
- **Evaluation Metric**: ROC AUC Score

---

## 📈 Results

| Model                | AUC Score       |
|---------------------|-----------------|
| **CatBoost**        | `<your_value>`  |
| **Random Forest**   | `<your_value>`  |

> 🔁 Replace `<your_value>` with the actual AUC results from your runs.

---

## 📁 Project Structure

```bash
├── train.csv                 # Training data
├── test.csv                  # Test data
├── submission.csv            # Submission format template
├── churn_prediction.ipynb    # Jupyter notebook with full workflow
├── README.md                 # This file
