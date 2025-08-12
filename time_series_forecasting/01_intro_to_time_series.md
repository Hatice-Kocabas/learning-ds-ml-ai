# Introduction to Time Series

## What is a Time Series?
A **time series** is a sequence of data points collected or recorded at specific time intervals.  
Examples:
- Daily stock prices
- Monthly sales numbers
- Hourly temperature readings

**Key point:** The order of data matters. The same values in a different order can have a completely different meaning.

---

## Components of a Time Series
1. **Trend** – The long-term movement in the data.
2. **Seasonality** – Patterns repeating at regular intervals (e.g., sales increase every December).
3. **Cyclic Patterns** – Irregular up and down movements (longer than seasonal).
4. **Noise** – Random variations that cannot be explained.

---

## Why Time Series is Special?
- Data is **dependent on time**.
- Past values often influence future values.
- Many models require stationary data (constant mean and variance over time).

---

## Example in Python
```python
import pandas as pd
import matplotlib.pyplot as plt

# Example: Load a time series dataset
url = "https://raw.githubusercontent.com/jbrownlee/Datasets/master/daily-min-temperatures.csv"
data = pd.read_csv(url, parse_dates=['Date'], index_col='Date')

# Show first rows
print(data.head())

# Plot
plt.figure(figsize=(10, 5))
plt.plot(data['Temp'], color='blue')
plt.title("Daily Minimum Temperatures")
plt.xlabel("Date")
plt.ylabel("Temperature (Celsius)")
plt.show()
