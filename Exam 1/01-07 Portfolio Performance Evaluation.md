# Portfolio Performance Evaluation

## Video ID: 2wtwY1sWffE
### Introduction to Portfolio Statistics
- **Shift from Individual Stocks to Portfolios**.
- A **portfolio** is a set of stock investments **allocated** based on a strategy.
- **Buy-and-Hold Strategy**:  
  - Invest in stocks with a set allocation.
  - Observe performance **over time**.
- **Total allocation must sum to 1.0**.

---

## Video ID: UweF-2-Tr9Y
### Calculating Portfolio Value (Step-by-Step)
1. **Start with a Prices DataFrame**:  
   - Columns = Stock Prices.
   - Rows = Daily values.
2. **Normalize Prices**:  
   - Divide each price by the **first row value**.
   - Converts prices into **cumulative returns**.
3. **Multiply by Allocations**:
   - Allocate percentages to each stock.
4. **Multiply by Starting Value**:
   - Converts into **cash values**.
5. **Compute Total Portfolio Value**:
   - **Sum** across all stock positions for each day.

---

## Video ID: 5EuA5qD9NfI
### Key Portfolio Statistics
- **Daily Returns**:  
  - First value is always **0**.
  - Exclude it from further calculations.
- **Important Metrics**:
  1. **Cumulative Return**  
  2. **Average Daily Return**  
  3. **Standard Deviation of Daily Return**  
  4. **Sharpe Ratio**  

**Formulas**:
- **Cumulative Return**:  
  \[ \frac{Final\ Portfolio\ Value}{Initial\ Portfolio\ Value} - 1 \]
- **Average Daily Return**:  
  \[ Mean(Daily\ Returns) \]
- **Standard Deviation**:  
  \[ Std(Daily\ Returns) \]

---

## Video ID: 5cqstpRndtI
### Sharpe Ratio - Risk-Adjusted Return
- Measures **return per unit of risk**.
- Helps compare portfolios with different **risk levels**.
- **Key Idea**: Higher **return** + Lower **risk** = Better performance.
- **Sharpe Ratio Formula**:  
  \[ S = \frac{Mean(R_p - R_f)}{StdDev(R_p - R_f)} \]

Where:
  - **R_p** = Portfolio Return.
  - **R_f** = Risk-Free Rate (e.g., Treasury Bonds).

- **Typical Risk-Free Rates**:
  - **LIBOR (London Interbank Offer Rate)**.
  - **3-Month Treasury Bill**.
  - **Often approximated as 0% in recent years**.

---

## Video ID: s0bxoD_0fAU
### Computing the Sharpe Ratio in Python
- Use **daily returns** instead of total return.
- **Formula**:
  \[ S = \frac{Mean(Daily\ Returns - Daily\ Risk\ Free\ Rate)}{StdDev(Daily\ Returns - Daily\ Risk\ Free\ Rate)} \]
- **Converting Annual Risk-Free Rate to Daily Rate**:
  \[ R_f(daily) = (1 + R_f(annual))^{\frac{1}{252}} - 1 \]

---

## Video ID: mykUMLWokkQ
### Sharpe Ratio Adjustments for Time Frame
- The **Sharpe ratio varies** based on how frequently you **sample data**.
- **Adjustment Factor (K)**:
  - **Daily Sampling**: \( K = \sqrt{252} \)
  - **Weekly Sampling**: \( K = \sqrt{52} \)
  - **Monthly Sampling**: \( K = \sqrt{12} \)
- **Annualized Sharpe Ratio**:
  \[ S_{annual} = K 	imes S_{daily} \]

---

## Video ID: lF-PNNje5I4
### Summary and Assignment
- **Portfolio Evaluation Metrics**:
  1. **Cumulative Return**.
  2. **Average Daily Return**.
  3. **Standard Deviation (Risk Measure)**.
  4. **Sharpe Ratio (Risk-Adjusted Return)**.

**Assignment**:
- Implement a function to **calculate portfolio statistics automatically**.

---

### Conclusion
- **Daily Portfolio Value Calculation** → Foundation for risk/return analysis.
- **Sharpe Ratio** → Key for comparing portfolios.
- **Python Implementation** → Automate and test trading strategies.

