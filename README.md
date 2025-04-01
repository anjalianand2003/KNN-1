# k-NN Classification: Universal Bank Loan Acceptance Prediction

This repository contains the R implementation of a **k-Nearest Neighbors (k-NN)** classifier on the **Universal Bank** dataset to predict whether a customer will accept a personal loan offer based on their demographics and behavior.

## 📊 Dataset Overview

The dataset contains information on **5000 customers**, including:

- Demographics (Age, Income, Family Size)
- Behavioral data (Credit Card usage, Online Banking)
- Previous loan responses

Only **9.6%** of the customers accepted a personal loan, resulting in a class imbalance — a key consideration during evaluation.

## 🔍 Problem Statement

Predict whether a customer will accept a personal loan using the k-NN classification algorithm. Evaluate model accuracy across different k values and assess predictions for a new customer profile.

## 🧠 Methodology

1. **Data Preparation**:
   - Converted categorical variables into factors.
   - Selected relevant features for classification.
   - Split data into training (70%) and testing (30%).

2. **Model Building (k-NN)**:
   - Tried k = 1, 3, 5, 7, 9.
   - Evaluated performance using confusion matrices.

3. **New Customer Prediction**:
   - Predicted loan acceptance for a new profile across all k values.

## 🏆 Best Model

| k | Accuracy |
|---|----------|
| 1 | 85.1%    |
| 3 | 85.9%    |
| 5 | 86.4%    |
| 7 | 86.6%    |
| 9 | **86.9%** |

- **Optimal k:** 9
- **New Customer Prediction (k=9):** Likely **NOT** to accept the loan.

## 🧑‍💻 Requirements

Install the following R packages:

```r
install.packages(c("gmodels", "caret", "class", "dplyr"))
