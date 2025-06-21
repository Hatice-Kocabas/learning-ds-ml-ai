# 🤖 Machine Learning Notes

This document provides a brief overview of fundamental machine learning concepts and algorithms.

---

## 🔹 What is Machine Learning?

Machine Learning is a subfield of Artificial Intelligence (AI) that enables systems to learn from data and make predictions or decisions without being explicitly programmed.

---

## 🔹 Categories of Machine Learning

| Type          | Description                              | Example Algorithms         |
| ------------- | ---------------------------------------- | -------------------------- |
| Supervised    | Learns from labeled data                 | Linear Regression, SVM     |
| Unsupervised  | Finds patterns in unlabeled data         | K-Means, PCA               |
| Reinforcement | Learns by trial and error (reward-based) | Q-Learning, Deep Q-Network |

---

## 🔹 Supervised Learning

- Model learns from the labeled datasets. For example house price prediction.

### 1. Regression

Predicts continuous values.

```python
# Example: Predict house prices
y = m * x + b
```

- **Common Algorithms**: Linear Regression, Ridge, Lasso, Decision Tree Regression
- **Metrics**: MSE, RMSE, MAE, R² Score (model eveluation metrics will be explicitly explained in upcoming documents.)

### 2. Classification

Predicts categorical classes.

```python
# Example: Spam or Not Spam
```

- **Common Algorithms**: Logistic Regression, KNN, SVM, Random Forest, XGBoost
- **Metrics**: Accuracy, Precision, Recall, F1 Score, Confusion Matrix, ROC AUC

---

## 🔹 Unsupervised Learning

-Model learns from the unlabeled datasets.

### 1. Clustering

Groups similar data points.

- **K-Means**, **DBSCAN**, **Hierarchical Clustering**

### 2. Dimensionality Reduction

Reduces features while preserving structure.

- **PCA**, **t-SNE**

---

## 🔹 Overfitting & Underfitting

- **Overfitting**: Model fits training data very well, does not perform well on unseen dataset (test set).
- **Underfitting**: Model is too simple, poor performance on both training and test data.

---

## 🔹 Train/Test Split

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)
```

---

## 🔹 Model Evaluation Metrics

| Task           | Metrics                                  |
| -------------- | ---------------------------------------- |
| Regression     | MSE, RMSE, MAE, R²                       |
| Classification | Accuracy, Precision, Recall, F1, ROC AUC |

---

## 🔹 Scikit-learn Workflow

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

---

## 🔹 Feature Scaling

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

---

## 🔹 Cross-Validation

```python
from sklearn.model_selection import cross_val_score

scores = cross_val_score(model, X, y, cv=5)
```

---

## 📌 Notes

- Understand the problem type (regression or classification)
- Always check for missing values and scale your features
- Evaluate multiple models and use cross-validation
- Avoid overfitting using regularization or simpler models

---
