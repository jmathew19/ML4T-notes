# Financial Data Analysis and Statistics - Detailed Lecture Notes

## Lecture 1: Global Statistics on Time Series Data

### Overview:
- **Time series data** represents stock prices, trading volumes, etc., over time.
- **Statistical analysis** helps identify trends and volatility in financial markets.
- Pandas provides built-in functions to compute global statistics efficiently.

### Key Global Statistics:
- **Mean (Average):** Sum of all values divided by the number of values.
- **Median:** Middle value when sorted.
- **Standard Deviation:** Measure of data spread around the mean.
- **Sum & Product:** Aggregate operations on data.
- **Mode:** Most frequently occurring value.

### Pandas Implementation:
```python
import pandas as pd

# Sample DataFrame with stock prices
df = pd.DataFrame({
    "SPY": [100, 102, 104, 106, 108],
    "XOM": [50, 51, 52, 53, 54],
    "GOOG": [1200, 1210, 1220, 1230, 1240],
    "GLD": [140, 142, 144, 146, 148]
})

# Compute global statistics
print(df.mean())   # Compute Mean
print(df.median()) # Compute Median
print(df.std())    # Compute Standard Deviation
print(df.sum())    # Compute Sum
print(df.mode())   # Compute Mode
```
---
## Lecture 2: Rolling Statistics

### Overview:
- **Rolling statistics** compute statistics over a moving window of time.
- Instead of a global statistic, a rolling statistic is applied to **subsets** of the dataset.
- Used in **financial analysis** to smooth out short-term fluctuations.

### Rolling Mean (Simple Moving Average - SMA):
- Computes the mean over a fixed window (e.g., 20 days).
- Reduces noise in stock prices by smoothing fluctuations.

### Code Implementation:
```python
df["RollingMean_20"] = df["SPY"].rolling(window=20).mean()
```

### Visualization:
- A rolling mean is **lagging** and follows the trend with a delay.
- **Traders use rolling averages** to determine **buy/sell signals** when prices cross averages.

---
## Lecture 3: Bollinger Bands

### Overview:
- Developed by **John Bollinger** in the 1980s.
- **Used to measure volatility** and identify overbought/oversold conditions.
- Consists of:
  - **Upper Band** = Rolling Mean + (2 * Standard Deviation)
  - **Lower Band** = Rolling Mean - (2 * Standard Deviation)

### Code Implementation:
```python
df["RollingMean"] = df["SPY"].rolling(window=20).mean()
df["UpperBand"] = df["RollingMean"] + 2 * df["SPY"].rolling(window=20).std()
df["LowerBand"] = df["RollingMean"] - 2 * df["SPY"].rolling(window=20).std()
```

### Interpretation:
- **Stock price touching the lower band** → Possible **buy signal**.
- **Stock price touching the upper band** → Possible **sell signal**.

---
## Lecture 4: Daily Returns

### Overview:
- Measures **how much a stock price changes daily**.
- Formula:
  ```math
  Daily Return = (Price_{t} / Price_{t-1}) - 1
  ```
- **Useful for comparing different stocks.**

### Code Implementation:
```python
df["DailyReturn"] = df["SPY"].pct_change()
```

### Visualization:
- **Daily returns are plotted as histograms** to analyze stock volatility.
- **Higher standard deviation** → More volatile stock.

---
## Lecture 5: Cumulative Returns

### Overview:
- Measures **total return** over a given period.
- Investors use it to analyze **long-term stock performance**.
- Formula:
  ```math
  Cumulative Return = (Price_{t} / Initial Price) - 1
  ```

### Code Implementation:
```python
df["CumulativeReturn"] = (df["SPY"] / df["SPY"].iloc[0]) - 1
```

### Interpretation:
- **Positive cumulative return** → Stock price is increasing over time.
- **Negative cumulative return** → Stock is losing value.

---
## Lecture 6: Handling Missing Data in Financial Data

### Overview:
- **Real-world financial data is not perfect.**
- **Causes of missing data:**
  - Market holidays (no trading).
  - Newly listed stocks (data starts late).
  - Delisted stocks (data stops abruptly).

### Handling Missing Data:
1. **Forward Fill (ffill)**:
   - Fills missing values using the **last known value**.
   ```python
   df.fillna(method='ffill', inplace=True)
   ```

2. **Backward Fill (bfill)**:
   - Fills missing values using the **next available value**.
   ```python
   df.fillna(method='bfill', inplace=True)
   ```

---
## Additional Topics

### 1. Histograms:
- Used to visualize **stock return distributions**.
- **Kurtosis** measures "fat tails" (extreme movements in stock prices).

### 2. Scatter Plots & Regression:
- **Beta (β)**: Measures stock volatility relative to the market.
- **Alpha (α)**: Measures stock performance relative to the market.

```python
import numpy as np
import matplotlib.pyplot as plt

# Scatter plot of SPY vs XOM daily returns
plt.scatter(df["SPY"], df["XOM"])
plt.xlabel("SPY Daily Return")
plt.ylabel("XOM Daily Return")
plt.title("Scatter plot of SPY vs XOM Returns")
plt.show()

# Linear regression (finding Beta & Alpha)
beta, alpha = np.polyfit(df["SPY"], df["XOM"], 1)
print(f"Beta: {beta}, Alpha: {alpha}")
```

---
## Summary

- **Pandas & NumPy** provide efficient tools for financial data analysis.
- **Rolling Statistics & Moving Averages** smooth out stock price fluctuations.
- **Bollinger Bands** help traders identify **buy/sell signals**.
- **Daily & Cumulative Returns** are key metrics for stock performance.
- **Data Cleaning** (handling missing values) is crucial for reliable analysis.

---

### Key Takeaways:
- Financial data **requires statistical techniques** for meaningful insights.
- Python (Pandas & NumPy) makes financial data analysis **efficient & scalable**.
- Understanding **rolling statistics, technical indicators, and risk measures** is essential for financial research.

