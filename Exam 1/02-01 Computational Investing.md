# Computational Investing Lecture Notes

## **Introduction to Computational Investing**
- The goal of this course is to help you understand the principles of **portfolio management**.
- Your motivation is likely **compensation**, which depends on the type of fund you manage and its performance.

---

## **Types of Investment Funds**
### **1. Exchange-Traded Funds (ETFs)**
- Traded like stocks.
- Prices are visible **intraday**.
- Represents a **basket of stocks or assets** (bonds, commodities, etc.).
- **Transparent**: Holdings are publicly available.
- **Liquid**: Can be easily bought and sold.

### **2. Mutual Funds**
- Similar to ETFs but have key differences:
  - Can **only be bought/sold at end of the day** (based on Net Asset Value).
  - Holdings are **disclosed quarterly**, making them **less transparent**.
  - Often track indices (S&P 500, large-cap stocks, etc.).

### **3. Hedge Funds**
- **Least transparent**:
  - Investors **sign agreements** that are often private.
  - Difficult to exit; funds require a **lock-in period** (months/years).
  - No requirement to **disclose holdings**, even to investors.
- Despite low transparency, they attract investors by showing strong performance.
![[Screenshot 2025-03-01 at 10.39.53 PM.png]]


---

## **Key Investment Terminology**
### **Liquidity**
- Ease of buying and selling an asset.
- Stocks and ETFs are **highly liquid**.
- **Higher trading volume** → Greater liquidity.

### **Market Capitalization (Cap)**
- **Total company value** = Stock price × Number of outstanding (available) shares.
- **Large-Cap Stocks**: Worth billions (e.g., Apple, Microsoft).
- **Small-Cap Stocks**: Worth much less, often higher risk.

---

## **Fund Manager Compensation**
### **1. ETFs & Mutual Funds**
- **Compensated via Expense Ratio** (percentage of Assets Under Management, AUM).
- **ETFs:** Typically **0.01% – 1%**.
- **Mutual Funds:** **0.5% – 3%** (higher fees due to active management).

### **2. Hedge Funds**
- Traditional **2 and 20 model**:
  - **2% of AUM** (management fee).
  - **20% of profits** (performance fee).
- Example:
  - A hedge fund manages **$100 million**.
  - The fund gains **15% ($15 million)**.
  - Compensation:
    - **2% of $100M = $2M**.
    - **20% of $15M = $3M**.
    - **Total earnings = $5M**.
- Recently, hedge funds have lowered fees (**1% and 10% is more common today**).

---

## **Types of Hedge Fund Investors**
1. **Individuals** (typically wealthy due to **minimum investment requirements**).
2. **Institutions** (e.g., retirement funds, university endowments).
3. **Funds of Funds** (investment firms that **pool** investor funds and allocate them across hedge funds).

### **Investor Considerations**
- **Track Record**: Historical performance over at least **5 years** is crucial.
- **Backtesting & Simulations**: Used when track record is unavailable.
- **Strategy Fit**: Investors seek diversification—your fund should **complement** existing holdings.

---

## **Hedge Fund Investment Strategies And Metrics**
### **1. Benchmark-Based Investing**
- **Goal:** Beat a specific benchmark (e.g., S&P 500).
- If the **market declines**, a fund can **still succeed** if it loses **less** than the benchmark.

### **2. Absolute Return Strategies**
- **Goal:** Generate **positive returns** regardless of market conditions.
- **Often involve long/short positions**:
  - Long: Buy stocks expected to rise.
  - Short: Bet against stocks expected to decline.
- Typically lower risk but also **lower returns** compared to benchmark strategies.

### **Performance Metrics**
- **Cumulative Return**: Measures total return over time.
- **Volatility**: Standard deviation of daily returns (lower is better).
- **Sharpe Ratio**:
  - Measures **risk-adjusted return**.
  - Formula: `(Avg. Daily Return - Risk-Free Rate) / Volatility`.
  - **Annualized using** `sqrt(252)` (252 trading days in a year).

---

## **Computing in Hedge Funds**
Hedge funds rely on **complex computational models** for trading and portfolio management.

### **Trading Algorithm**
- **Compares live portfolio to target portfolio**.
- Adjusts holdings by issuing buy/sell orders.
- **Key Challenge**: Avoid market impact (e.g., placing a large order may move prices).

### **Portfolio Optimization**
- Uses **forecast models** to predict stock prices.
- Portfolio optimizers balance **risk vs. return**.
- Inputs:
  - **Historical stock data** (open, high, low, close, volume).
  - **Current portfolio holdings** (reducing excessive trading).
  - **Stock correlations** (diversification considerations).

### **Machine Learning in Hedge Funds**
- **Forecasting Models** predict **future price movements**.
- Uses **proprietary data** and historical trends.
- Common techniques:
  - **Statistical modeling**.
  - **Deep learning** for pattern recognition.
  - **Sentiment analysis** (e.g., using news and social media).

---

## **Summary**
- **Investment Funds:** ETFs, Mutual Funds, Hedge Funds.
- **Liquidity & Market Cap:** Determines trading ease and firm valuation.
- **Fund Manager Compensation:** ETFs/mutual funds use **expense ratios**, hedge funds use **performance-based incentives**.
- **Investor Expectations:** Require strong **track records**, **backtesting**, and **clear strategy rationale**.
- **Computational Hedge Fund Strategies:**
  - **Algorithmic trading** minimizes market impact.
  - **Portfolio optimization** balances risk and return.
  - **Machine learning** improves stock price forecasting.

### **Next Steps**
- Learn **portfolio construction** and **risk management**.
- Explore **algorithmic trading strategies**.
- Apply **machine learning to financial data analysis**.

