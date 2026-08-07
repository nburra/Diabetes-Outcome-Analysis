# Diabetes Risk Prediction Analysis

## Overview

This project develops a machine learning pipeline to analyze patient health indicators and predict diabetes outcomes using clinical and demographic features.

The analysis explores relationships between physiological factors such as glucose levels, BMI, blood pressure, insulin, and age to understand key drivers associated with diabetes risk.

Multiple classification models were evaluated, including Support Vector Machines (SVM), K-Nearest Neighbors (KNN), and Decision Trees, to identify the most effective approach for diabetes prediction.

The goal of this project is to demonstrate how healthcare data analytics and predictive modeling can support early risk identification and data-driven clinical decision-making.

---

# Business Problem

Diabetes is a widespread chronic condition where early detection and risk assessment can improve patient outcomes.

Healthcare organizations face challenges including:

- Identifying high-risk patients efficiently
- Understanding relationships between patient characteristics and diabetes outcomes
- Supporting preventative care through predictive analytics

This project investigates:

> **Can machine learning models accurately predict diabetes outcomes based on patient health indicators?**

---

# Dataset

The analysis uses a diabetes dataset containing patient-level health measurements.

## Features Analyzed

Key predictors include:

- Glucose levels
- Blood pressure
- Body Mass Index (BMI)
- Insulin levels
- Skin thickness
- Age
- Pregnancy history
- Diabetes pedigree function

Target variable:

- Diabetes outcome classification

---

# Analytical Approach

## 1. Data Exploration & Cleaning

Initial exploratory data analysis was performed to understand:

- Dataset structure
- Feature distributions
- Missing values
- Relationships between health indicators

Data preprocessing included:

- Identifying invalid zero values
- Handling missing values using median imputation
- Preparing features for machine learning models

Tools:

- Python
- Pandas
- NumPy

---

# 2. Exploratory Data Analysis

Analyzed relationships between clinical variables including:

## Blood Pressure Analysis

Examined blood pressure distributions to identify common patient patterns and detect invalid measurements.

## BMI & Blood Pressure Relationship

Performed correlation analysis to evaluate relationships between body composition and cardiovascular indicators.

Key finding:

- Higher BMI generally correlated with increased blood pressure, although variation existed across patient groups.

---

# 3. Machine Learning Pipeline

A supervised machine learning pipeline was developed to classify diabetes outcomes.

## Data Processing

Steps included:

- Train/test split
- Feature normalization
- Data preprocessing
- Model evaluation

---

# Models Evaluated

## Support Vector Machine (SVM)

A Support Vector Machine classifier was optimized using:

- GridSearchCV
- 5-fold cross-validation
- Hyperparameter tuning

Results:

- Highest predictive performance among evaluated models
- Strong consistency between training and testing performance

---

## K-Nearest Neighbors (KNN)

Evaluated as a distance-based classification approach.

Performance:

- Achieved approximately 74% accuracy
- Demonstrated reliable classification performance

---

## Decision Tree

Evaluated for interpretability and rule-based prediction.

Performance:

- Lower accuracy compared to SVM and KNN
- Lower F1 score for diabetes-positive classification

---

# Model Performance

| Model | Accuracy | Evaluation |
|---|---|---|
| Support Vector Machine | ~78% | Best overall performance |
| K-Nearest Neighbors | ~74% | Strong baseline model |
| Decision Tree | ~69% | Lower predictive performance |

---

# Key Insights

## Clinical Factors Influence Diabetes Risk

Patient health indicators such as glucose, BMI, insulin, and age provide meaningful signals for predicting diabetes outcomes.

---

## Machine Learning Can Support Risk Identification

The SVM model demonstrated that predictive analytics can help identify individuals at increased risk of diabetes based on available clinical information.

---

## Predictive Models Require Clinical Validation

Although the model showed promising performance, additional improvements and validation using larger clinical datasets would be necessary before healthcare deployment.

---

# Technologies

## Programming

- Python

## Data Analysis

- Pandas
- NumPy

## Machine Learning

- Scikit-learn
- Support Vector Machines
- K-Nearest Neighbors
- Decision Trees
- GridSearchCV

## Visualization

- Matplotlib

---

# Repository Structure

```
Diabetes-Outcome-Analysis/

│
├── README.md
│
├── diabetes.csv
│
└── diabetes_outcome_analysis.ipynb
```

---

# Skills Demonstrated

- Healthcare Analytics
- Predictive Modeling
- Hyperparameter Optimization

---

# Future Improvements

Potential extensions include:

- Testing additional models such as XGBoost, and Neural Networks
- Using larger clinical datasets for validation

---

# Project Impact

This project demonstrates how machine learning can transform healthcare data into predictive insights.

By combining exploratory analysis, preprocessing techniques, and classification models, this analysis provides a framework for identifying diabetes risk factors and supporting data-driven healthcare decision-making.
