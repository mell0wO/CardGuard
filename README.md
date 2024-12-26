# **Credit Card Fraud Detection**

## **Overview**
This project aims to build and evaluate machine learning models for detecting fraudulent credit card transactions. Using a dataset of credit card transactions, the goal is to predict whether a transaction is fraudulent (Class = 1) or non-fraudulent (Class = 0). The project implements four popular classification algorithms: Logistic Regression, Decision Tree, Random Forest, and Support Vector Machine (SVM), and compares their performance using key evaluation metrics.

---

## **Table of Contents**
- [Project Overview](#overview)
- [Dataset](#dataset)
- [Model Development](#model-development)
- [Results](#results)
- [Conclusion](#conclusion)
- [Setup](#setup)

---

## **Dataset**
The dataset used for this project is from [Kaggle: Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). It contains 284,807 transactions, with 492 frauds, making the dataset highly imbalanced.

Key features include:
- **Time**: Elapsed time (in seconds) from the first transaction in the dataset.
- **V1-V28**: 28 anonymized features resulting from PCA (Principal Component Analysis).
- **Amount**: Transaction amount.
- **Class**: Class label where 1 represents a fraudulent transaction, and 0 represents a non-fraudulent transaction.

---

## **Model Development**

In this project, four machine learning models were developed and evaluated:

1. **Logistic Regression**:  
   A simple, interpretable model for binary classification. Logistic Regression is widely used for its simplicity and effectiveness in scenarios where the data has a linear decision boundary.

2. **Decision Tree**:  
   A model that splits the data into decision nodes based on feature values. It works by recursively splitting the data at each node based on the feature that provides the best separation (measured by metrics like Gini impurity or entropy). Decision Trees can capture non-linear relationships but may overfit if not tuned properly.

3. **Random Forest**:  
   An ensemble method that combines multiple decision trees to reduce overfitting. Random Forest creates a collection of decision trees trained on random subsets of data, with each tree making predictions independently. The final prediction is based on the majority vote (classification) or the average (regression). This approach improves the model's accuracy and robustness compared to a single decision tree.

4. **Support Vector Machine (SVM)**:  
   A powerful classifier that works well for complex, non-linear decision boundaries. SVM constructs a hyperplane in a high-dimensional space that best separates different classes. It uses kernel tricks to handle non-linearity, making it highly effective for problems where the data is not linearly separable.

---

## **Steps**

### 1. **Data Preprocessing:**
   - Handle **missing values**: Identified and addressed any missing or null values in the dataset to ensure the models are trained on complete data.
   - Address **imbalanced classes**: The dataset had imbalanced classes, with a disproportionate number of non-fraudulent transactions. Techniques like downsampling the majority class (non-fraudulent transactions) were used to balance the dataset.
   - Apply **scaling techniques**: The features were scaled using the **PowerTransformer** to handle skewness and ensure that the data follows a normal distribution, which is often required for some machine learning algorithms.

### 2. **Model Training and Evaluation:**
   - **Train models**: The models were trained using the training set (`X_train`, `y_train`) to learn the patterns in the data.
   - **Evaluate models**: The performance of the models was evaluated using the test set (`X_test`, `y_test`).
   - **Use classification metrics**: Key classification metrics such as **accuracy**, **precision**, **recall**, **F1-score**, and the **confusion matrix** were calculated to evaluate the models' performance and identify how well they handled fraud detection.

### 3. **Model Comparison:**
   - **Compare performance**: The performance of all four models (Logistic Regression, Decision Tree, Random Forest, and Support Vector Machine) was compared using the evaluation metrics mentioned above. This helped determine the most effective model for detecting fraud in credit card transactions.

---

## **Results**

### **Evaluation Metrics:**

- **Logistic Regression**:
  - Achieved **high accuracy** but was **less reliable on the test data**. This is likely due to its linear nature, which struggles to capture the complexities of the dataset, especially in cases of non-linear decision boundaries.
  
- **Decision Tree**:
  - Demonstrated **overfitting on the training data**, suggesting that the model learned too well from the training set and failed to generalize effectively to the test set. This overfitting implies a need for **parameter tuning** (e.g., pruning, adjusting max depth).

- **Random Forest**:
  - **Best-performing model** overall, showing **high accuracy** and **balanced precision and recall**. The ensemble approach of Random Forest helped to mitigate overfitting and provided a robust model for fraud detection.

- **Support Vector Machine (SVM)**:
  - Achieved **competitive performance** but was **sensitive to feature scaling** and the choice of **kernel**. SVM's performance could vary significantly based on how the features are scaled and the choice of kernel parameters.

---

## **Conclusion**
Random Forest emerged as the best model for predicting fraudulent transactions, providing the best balance of accuracy and robustness.

---

## **Setup**

### Prerequisites
To get started with this project, ensure that you have Python installed (preferably Python 3.6 or higher).

### Install Required Libraries
To install the necessary libraries, use the following command:

```bash
pip install -r requirements.txt




