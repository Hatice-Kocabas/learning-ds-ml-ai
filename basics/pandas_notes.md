# 📌 Pandas Notes for Data Science

This file contains quick notes and code examples for learning Pandas — the most popular data manipulation library in Python.

---

## 🔹 Importing Pandas

```python
import pandas as pd
```

---

## 🔹 Core Data Structures

### Series

```python
s = pd.Series([1, 3, 5, 7])
print(s)
```

### DataFrame

```python
data = {
    "name": ["Alice", "Bob", "Charlie"],
    "age": [25, 30, 35],
    "city": ["NY", "LA", "Chicago"]
}
df = pd.DataFrame(data)
print(df.head())

# pandas data frames can be think as a table whch contains columns and rows. 
```

---

## 🔹 Reading Data

```python
df = pd.read_csv("data.csv") #reading data from csv file
```

---

## 🔹 Basic Data Exploration

```python
df.head()       # first 5 rows
df.head(7)      #first seven row
df.tail()       # last 5 rows
df.info()       # summary of dataframe
df.describe()   # statistical summary
df.columns      # column names
df.shape        # dimensions
```

---

## 🔹 Selecting Data

```python
df["age"]           # select one column (Series)
df[["name", "city"]] # select multiple columns (DataFrame)
df.loc[0]           # select first row by label
df.iloc[0]          # select first row by position
```

---

## 🔹 Filtering Data

```python
df[df["age"] > 30]          # rows where age > 30
df[(df["age"] > 20) & (df["city"] == "NY")]
```

---

## 🔹 Adding / Modifying Columns

```python
df["new_col"] = df["age"] * 2
df["age_plus_5"] = df["age"] + 5
```

---

## 🔹 Handling Missing Data

```python
df.isnull().sum()            # count missing values per column
df.dropna(inplace=True)      # drop rows with missing values
df.fillna(0, inplace=True)   # fill missing values with 0
```

---

## 🔹 Grouping and Aggregation

```python
df.groupby("city")["age"].mean()
df.groupby("city").agg({"age": ["mean", "max"], "new_col": "sum"})
```

---

## 🔹 Sorting Data

```python
df.sort_values(by="age", ascending=False)
```

---

## 🔹 Exporting Data

```python
df.to_csv("output.csv", index=False)
```

---

## 📌 Notes

- Pandas is essential for EDA (Exploratory Data Analysis).
- Practice selecting, filtering, grouping, and handling missing data.
- Check: `numpy-pandas.ipynb` for applied examples combining NumPy and Pandas.

---
