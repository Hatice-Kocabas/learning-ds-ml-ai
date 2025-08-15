# 03 - Moving Average (MA) in Time Series

## What is Moving Average?

Moving Average is a simple method to smooth out short-term fluctuations and highlight longer-term trends or cycles in time series data.

It calculates the average of data points over a fixed number of previous periods (window size).

---

## Why use Moving Average?

- Reduces noise and volatility.
- Helps identify trends.
- Useful for forecasting and anomaly detection.

---

## Types of Moving Averages

- **Simple Moving Average (SMA):** Equal weighting to all points in the window.
- **Weighted Moving Average (WMA):** More weight to recent data points.
- **Exponential Moving Average (EMA):** Weights decrease exponentially for older data.

---

## Simple Moving Average Example in Python

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
url = "https://raw.githubusercontent.com/jbrownlee/Datasets/master/daily-min-temperatures.csv"
data = pd.read_csv(url, parse_dates=['Date'], index_col='Date')

# Calculate 7-day Simple Moving Average
data['SMA_7'] = data['Temp'].rolling(window=7).mean()

# Plot original and SMA
plt.figure(figsize=(12,6))
plt.plot(data['Temp'], label='Original')
plt.plot(data['SMA_7'], label='7-day SMA', color='orange')
plt.title('Daily Minimum Temperatures with 7-day Moving Average')
plt.xlabel('Date')
plt.ylabel('Temperature (°C)')
plt.legend()
plt.show()

```

## Key Points

- Window size choice impacts smoothness: larger window = smoother curve.

- Moving averages lag behind actual data; they don’t predict future points.

- Useful in combination with other analysis methods.
