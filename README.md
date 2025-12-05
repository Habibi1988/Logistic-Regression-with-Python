# 📞 Logistic Regression Model for Customer Churn Prediction

## Project Overview

This project implements a **Logistic Regression classifier** using Python and Scikit-learn to predict customer churn for a telecommunications company. The primary goal is to identify customers at high risk of leaving the company so that proactive retention efforts can be deployed.

This analysis follows a standard machine learning workflow, including data preprocessing, feature scaling, model training, and performance evaluation using key classification metrics.

## 🎯 Objectives

* **Implement** Logistic Regression for a binary classification task.
* **Demonstrate** essential data preprocessing steps, including feature scaling using `StandardScaler`.
* **Evaluate** model performance using the Log Loss metric, focusing on probability accuracy.
* **Interpret** the influence of individual features (coefficients) on the prediction outcome.

## 📊 Dataset

The data used is a historical customer dataset provided by IBM/Coursera, detailing various customer preferences, services opted, and personal information.

* **Source:** IBM Developer Skills Network
* **Target Variable:** `churn` (0: Stayed, 1: Churned)
* **Initial Features:** `tenure`, `age`, `address`, `income`, `ed`, `employ`, `equip`, etc.

## 🛠️ Key Steps & Model Interpretation

### 1. Data Preparation
The dataset was loaded and preprocessed. The target variable (`churn`) was converted to the required integer format.

### 2. Feature Standardization
All numerical input features (`X`) were standardized using `StandardScaler` to ensure they contribute equally to the model, preventing features with larger scales (like income) from dominating the distance calculations.

### 3. Model Training & Evaluation
The data was split (80% Train, 20% Test) and a `LogisticRegression` model was trained.

| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **Log Loss (Original 7-Feature Model)** | **[0.6257718410257236]** | A lower value indicates better probability prediction accuracy. |

### 4. Feature Coefficient Analysis
The model's coefficients were analyzed to understand which factors drive churn:

* **Positive Coefficients:** Increase the likelihood of churn (e.g., perhaps high equipment use).
* **Negative Coefficients:** Decrease the likelihood of churn (e.g., longer tenure).

## 💻 How to Run the Project

### Prerequisites

To run the Jupyter Notebook (`Logistic Regression with Python.ipynb`), you need the following Python libraries:

```text
numpy
pandas
scikit-learn
matplotlib
