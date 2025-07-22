# 🌳 Decision Trees – Basics

Decision Trees are a type of **supervised learning algorithm** used for both **classification** and **regression** tasks.

---

## 🧠 How They Work

- A decision tree splits the dataset into smaller and smaller subsets while at the same time creating a tree-like structure.
- It chooses the best **feature** to split at each step using **impurity metrics** (like Gini or Entropy for classification).

---

## 📊 Key Terminologies

- **Root Node**: The top-most node that represents the entire dataset.
- **Internal Node**: Nodes that split into further sub-nodes.
- **Leaf Node**: The final output or decision.

---

## 🧮 Splitting Criteria

| Criterion     | Used For        | Formula / Notes                          |
|--------------|------------------|------------------------------------------|
| Gini Index   | Classification   | Lower Gini = better split                |
| Entropy      | Classification   | Based on Information Gain                |
| MSE / MAE    | Regression       | Mean Squared / Absolute Error            |

---

## 🪓 Overfitting in Decision Trees

Decision trees can **overfit** the training data, especially if the tree grows very deep.

**To prevent overfitting:**
- Set a maximum depth (`max_depth`)
- Set minimum samples per leaf (`min_samples_leaf`)
- Use pruning techniques

---

## ✅ Pros and Cons

**Pros**
- Easy to understand and visualize
- No need for feature scaling
- Can handle both numerical and categorical data

**Cons**
- Prone to overfitting
- Can be unstable to small variations in data

---

## 🧪 Common Hyperparameters (Sklearn)

```python
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier(
    criterion="gini",       # or "entropy"
    max_depth=5,
    min_samples_split=10,
    random_state=42
)
