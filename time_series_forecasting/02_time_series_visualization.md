# 02 - Time Series Visualization

## Why Visualization Matters
Before building any time series model, it’s important to **visualize** the data:
- Identify **trends** (upward/downward movement over time).
- Detect **seasonality** (repeated patterns).
- Spot **outliers** or anomalies.
- Understand **data distribution** over time.

---

## 1. Line Plot (Basic)
The most common way to visualize time series data.

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load example dataset
url = "https://raw.githubusercontent.com/jbrownlee/Datasets/master/daily-min-temperatures.csv"
data = pd.read_csv(url, parse_dates=['Date'], index_col='Date')

# Plot basic line chart
plt.figure(figsize=(10, 5))
plt.plot(data['Temp'], color='blue')
plt.title("Daily Minimum Temperatures")
plt.xlabel("Date")
plt.ylabel("Temperature (°C)")
plt.show()



```
## 2. Seasonal Plot (Boxplot by Month)
Helps to visualize patterns within a season (e.g., months or days).

```python
import seaborn as sns

# Extract month from the date index
data['Month'] = data.index.month

# Plot monthly distribution
plt.figure(figsize=(10, 5))
sns.boxplot(x='Month', y='Temp', data=data)
plt.title("Monthly Temperature Distribution")
plt.xlabel("Month")
plt.ylabel("Temperature (°C)")
plt.show()


```
## 3. Interactive Plot (Using Plotly)
Useful for zooming and exploring details.


```python
import plotly.express as px

fig = px.line(
    data,
    x=data.index,
    y='Temp',
    title="Daily Minimum Temperatures"
)
fig.show()


```

## Key Tips

- Always start with a simple line plot to understand the overall pattern.

- Use boxplots to explore seasonal variations.

- Interactive plots are great for deep exploration but static plots are better for quick overviews.

- Visualization often reveals problems (e.g., missing data, unusual spikes) before modeling.




