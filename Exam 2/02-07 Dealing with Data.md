# Lecture: Computational Investing and Financial Data

## Video ID: n8lhpKoJUt4
### Introduction to Financial Data
- **Importance of Data**:
  - Core data in computational investing includes **historical price** and **volume**.
  - This lesson focuses on **understanding and analyzing financial data**.

## Video ID: 8uxsIBCJlOc
### Aggregation of Financial Data
- **Tick Data**:
  - Represents **individual transactions**.
  - Each tick consists of:
    - **Price**
    - **Volume**
- ![[Screenshot 2025-03-05 at 1.32.39 PM.png]]
  - Transactions occur **whenever a buy and sell match**, not at fixed intervals.
- **Data Consolidation**:
  - Tick data is aggregated into **minute-by-minute or hourly data**.
  - Commonly used metrics:
    - **Open**: First transaction price in the period.
    - **High**: Highest price in the period.
    - **Low**: Lowest price in the period.
    - **Close**: Last transaction price in the period.
    - **Volume**: Total shares traded in the period.
    - ![[Screenshot 2025-03-05 at 1.34.26 PM.png]]
- **Daily Data Usage**:
  - The course primarily uses **daily closing data**.
  - Analyzing smaller time frames requires **faster computing and larger datasets**.
---
## Price Anomaly

![[Screenshot 2025-03-05 at 1.35.35 PM.png]]

Sometimes prices can have abnormalities because stock splits

## Video ID: 6o4Aecb6Xiw
### Stock Splits and Adjusted Close Prices
- **Why Do Stocks Split?**
  - When a stock's price is **too high**, it becomes less accessible.
  - Example:
    - A $500 stock means **100 shares cost $50,000**.
    - **Options contracts** also become more expensive.
  - A **stock split** reduces the price while increasing the number of shares.
    - *Example*: A **2-for-1 split** turns **one $300 share into two $150 shares**.
- **Impact on Data Analysis**:
  - Raw stock price data **does not reflect splits**, leading to misleading trends.
  - Algo might incorrectly decide to short at that stock and reap huge benefits, but  this is wrong the price didn't go down 
  - **Solution**: **Adjusted Close Prices**.
    - Adjusts past prices to create a **continuous price timeline**.
    - Example: If a stock split **2-for-1**, all previous prices are divided by 2.
    - **Ensures accurate price comparisons over time**.
![[Screenshot 2025-03-05 at 1.42.22 PM.png]]

![[Screenshot 2025-03-05 at 1.46.12 PM.png]]


## Video ID: Bn-deRD_F6o
### Dividends and Stock Prices
- **Effect of Dividends**:
  - Companies distribute earnings as **dividends** (e.g., $1 per share).
  - Stock prices often rise before the **ex-dividend date** and drop afterward.
- **Adjusted Close Prices for Dividends**:
  - Adjust historical prices by the **dividend percentage** to maintain a smooth trend.
  - Ensures **price charts accurately reflect total return**.

![[Screenshot 2025-03-05 at 1.50.22 PM.png]]

## Video ID: RCB2hkiwqnA
### Handling Dividend Adjustments
- **Price Adjustments**:
  - Adjusting prices for dividends **removes artificial price drops**.
  - Historical prices are **lowered by the dividend percentage** to create a **smooth dataset**.
- **Key Considerations**:
  - **Adjusted Close prices** reflect both **dividends and splits**.
  - When using external data sources (Yahoo Finance, Google Finance), **adjustments may change over time**.![[Screenshot 2025-03-05 at 1.51.01 PM.png]]
- 

## Video ID: Vj2m3XWCoOw
### Avoiding Bias in Backtesting Strategies
- **Backtesting**:
  - Simulating **historical trading** to evaluate a strategy.
  - Uses **historical stock data** to check past performance.
- **Survivorship Bias**:
  - A **common mistake** is using today's **S&P 500 stock list** for past strategies.
  - Some stocks **no longer exist** due to mergers, bankruptcies, etc.
  - *Example*: From **2007 to 2009, 68 stocks were removed** from the S&P 500.
  - **Solution**: Use **historical index membership data** to avoid bias.


## Video ID: oR3yxesPe6g
### Key Takeaways
- **Financial Data Types**:
  - **Tick Data**: Real-time transactions.
  - **Minute/Hourly Aggregates**: Simplified summaries.
  - **Daily Data**: Used for long-term analysis.
- **Stock Adjustments**:
  - **Stock splits** → Price is divided to maintain accuracy.
  - **Dividends** → Adjustments remove artificial price drops.
- **Backtesting Caution**:
  - Avoid **survivorship bias**.
  - Use **accurate historical index data**.

