# **Credit Card Fraud Detection**

## **Overview**
This project aims to build and evaluate machine learning models for detecting fraudulent credit card transactions. Using a dataset of credit card transactions, the goal is to predict whether a transaction is fraudulent (Class = 1) or non-fraudulent (Class = 0). The project implements four popular classification algorithms: Logistic Regression, Decision Tree, Random Forest, and Support Vector Machine (SVM), and compares their performance using key evaluation metrics.

---

## **Table of Contents**
- [Project Overview](#overview)
- [Dataset](#dataset)
- [Setup](#setup)
- [Model Development](#model-development)
- [Results](#results)
- [Conclusion](#conclusion)
- [Next Steps](#next-steps)
- [License](#license)

---

## **Dataset**
The dataset used for this project is from [Kaggle: Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). It contains 284,807 transactions, with 492 frauds, making the dataset highly imbalanced.

Key features include:
- **Time**: Elapsed time (in seconds) from the first transaction in the dataset.
- **V1-V28**: 28 anonymized features resulting from PCA (Principal Component Analysis).
- **Amount**: Transaction amount.
- **Class**: Class label where 1 represents a fraudulent transaction, and 0 represents a non-fraudulent transaction.

---

## **Setup**

### Prerequisites
To get started with this project, ensure that you have Python installed (preferably Python 3.6 or higher).

### Install Required Libraries
To install the necessary libraries, use the following command:

```bash
pip install -r requirements.txt
