# 🌳 Random Forest Classifier - Basics

## 🔍 What is Random Forest?

Random Forest is an **ensemble learning algorithm** that builds multiple decision trees and merges them together to get a more accurate and stable prediction.

- It works well for both classification and regression problems.
- It reduces **overfitting** that individual decision trees usually suffer from.
- Uses **bagging** (Bootstrap Aggregating).

---

## 📦 Key Parameters

- `n_estimators`: Number of trees in the forest.
- `max_depth`: Maximum depth of each tree.
- `random_state`: For reproducibility.
- `max_features`: Number of features to consider when looking for the best split.

---

## ✅ Advantages

- Handles missing values well.
- Good at handling large datasets.
- Reduces variance (compared to decision trees).

---

## 📊 Use Case: Titanic Dataset

### Features used:
- `Pclass` (passenger class)
- `Sex`
- `Age`
- `Fare`

### Target:
- `Survived`

---

## 📈 Performance Metrics

Use:
- `accuracy_score`
- `classification_report` (includes precision, recall, f1-score)

---

## 🧠 Tips
- Scale is not very important for Random Forests.
- You can extract **feature importances** using `.feature_importances_`.

```python
model.feature_importances_
