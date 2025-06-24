# 📊 ML Evaluation Metrics

This document provides a concise overview of the most commonly used machine learning evaluation metrics for regression and classification models.

---

## 🧮 1. Regression Metrics

Used to evaluate models that predict **continuous values**.

| Metric              | Formula / Description                              |
|---------------------|-----------------------------------------------------|
| **MSE**             | Mean Squared Error: average of squared errors       |
| **RMSE**            | Root of MSE                                         |
| **MAE**             | Mean Absolute Error: average of absolute errors     |
| **R² Score**        | Coefficient of determination (0 to 1, higher is better) |

```python
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score

mse = mean_squared_error(y_true, y_pred)
rmse = mse**0.5
mae = mean_absolute_error(y_true, y_pred)
r2 = r2_score(y_true, y_pred)
```

---

## 🔠 2. Classification Metrics

Used for **categorical predictions** (e.g. spam/ham, yes/no).

### ✅ Accuracy

> Correct predictions / Total predictions  
⚠️ May be misleading in imbalanced datasets.

```python
from sklearn.metrics import accuracy_score
accuracy = accuracy_score(y_true, y_pred)
```

### 📦 Confusion Matrix

|                | Predicted: No | Predicted: Yes |
|----------------|----------------|----------------|
| **Actual: No** | True Negative  | False Positive |
| **Actual: Yes**| False Negative | True Positive  |

```python
from sklearn.metrics import confusion_matrix
conf_matrix = confusion_matrix(y_true, y_pred)
```

---

### 📊 Precision, Recall, F1 Score

| Metric     | Formula                            | Best Use Case                          |
|------------|-------------------------------------|----------------------------------------|
| Precision  | TP / (TP + FP)                     | When False Positives are costly        |
| Recall     | TP / (TP + FN)                     | When False Negatives are costly        |
| F1 Score   | Harmonic mean of Precision & Recall| Balance between Precision and Recall   |

```python
from sklearn.metrics import precision_score, recall_score, f1_score

precision = precision_score(y_true, y_pred)
recall = recall_score(y_true, y_pred)
f1 = f1_score(y_true, y_pred)
```

---

### 📈 ROC Curve & AUC

- ROC = Receiver Operating Characteristic  
- AUC = Area Under the Curve  
- AUC ranges from 0.5 (random) to 1.0 (perfect)

```python
from sklearn.metrics import roc_auc_score

auc = roc_auc_score(y_true, y_proba)
```

> Note: `y_proba` should be predicted probabilities, not class labels

---

## 📝 Notes

- Always choose metrics **based on your problem**
- For imbalanced classification → prefer Precision, Recall, F1, AUC over Accuracy
- For regression → look at both **error magnitude (MAE, RMSE)** and **fit quality (R²)**

---
