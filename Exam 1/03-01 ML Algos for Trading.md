# Machine Learning Algorithms for Trading

## Video ID: 8hKvJPgAeHQ
### Introduction to Machine Learning in Trading
- Hedge funds and financial institutions use **machine learning** to predict future prices of stocks or other assets.
- Machine learning allows a **data-centric approach** to predictive models.
- Unlike traditional models, machine learning algorithms **adapt to patterns** in historical data.

---

## Video ID: NVWzWfglblo
### What Problem Does Machine Learning Solve?
- **Machine learning models** take in observations (X) and produce predictions (Y).
- Example in finance:
  - **X** = Features of stocks (e.g., Bollinger Bands, PE ratio, momentum).
  - **Y** = Future stock price prediction.
- Some models use mathematical formulas (e.g., **Black-Scholes model**), while **machine learning models use data-driven learning**.
![[Screenshot 2025-03-01 at 10.02.12 PM.png]]
---

## Video ID: 9Ejng7fbBAc
### Supervised Regression Learning
- **Regression** = Making a numerical prediction (as opposed to classification, which assigns labels).
- **Supervised learning** = Training the model with **X and known Y values**.
- Common **supervised regression algorithms**:
  - **Linear Regression**: Finds parameters for a model (**parametric** learning).
  - **K-Nearest Neighbors (KNN)**: Stores all training data and makes predictions based on the closest examples (**instance-based** learning).
  - **Decision Trees**: Splits data into decision rules.
  - **Decision Forests**: Uses multiple decision trees to improve accuracy.

---

## Video ID: VmPGyM-mun4
### Applying Machine Learning to Stock Data
- **Stock features (X) are recorded daily**, including:
  - Bollinger Bands
  - PE Ratio
  - Momentum indicators
- Future stock prices (Y) are used as labels.
- The **model is trained on past X-Y pairs**, then used to make predictions on unseen data.

![[Pasted image 20250301220836.png]]

---

## Video ID: mmshTSthMms
### Machine Learning in a FinTech Company
- **Lucena Research** builds financial models with machine learning.
- Steps to train a **predictive model**:
  1. Select **factors (X)** (e.g., Bollinger Bands, PE Ratio).
  2. Define the **target variable (Y)** (future price or relative change).
  3. Choose a **time period and stock universe**.
  4. Train the **machine learning algorithm** (e.g., KNN, regression, decision trees).
  5. Use the trained model to **predict future prices**.

![[Screenshot 2025-03-01 at 10.10.27 PM.png]]



---

## Video ID: GVOEnkjmBZU
### Forecasting Stocks with Machine Learning
- Example: **QuantDesk** software for forecasting.
- Uses **genetic algorithms** to optimize which factors (X) matter most.
- Users can configure:
  - **Forecast horizon** (1 week, 1 month, etc.).
  - **Lookback period** (e.g., last 3 months of stock data).
- Predictions include **confidence levels**, based on **standard deviation of similar past cases**.


---

## Video ID: VdcykrQTO80
### Evaluating Forecast Accuracy – Backtesting
- **Backtesting** = Testing a trading strategy on historical data.
- Steps:
  1. Train the model **only on past data** (simulate real-time predictions).
  2. Generate **trade orders** based on predictions.
  3. Simulate **portfolio performance** with metrics like:
     - **Sharpe Ratio**
     - **Total Return**
  4. Compare performance against a **benchmark (e.g., S&P 500)**.

![[Screenshot 2025-03-01 at 10.12.00 PM.png]]
![[Screenshot 2025-03-01 at 10.12.24 PM.png]]

---

## Video ID: oq25gWxMxKM
### Limitations of Regression-Based Forecasting
- **Predictions are noisy and uncertain**.
- **Difficult to assess confidence levels** in individual forecasts.
- **Holding period & allocation challenges**: Not always clear when to exit trades.
- **Alternative approach**: **Reinforcement Learning**, where models learn **trading policies** instead of predicting prices.

---

## Video ID: mBJ2qrjQaEg
### Course Structure for Machine Learning Trading
- Training **machine learning models** on stock data from 2009.
- Comparing **different algorithms** (KNN, regression, etc.).
- Testing model performance on **2010-2011 stock data**.
- Generating **trade orders** based on predictions.
- Evaluating performance using **Sharpe Ratio and Total Return**.

---

### Conclusion
- Machine learning is widely used in **quantitative trading**.
- **Supervised learning** helps forecast stock prices using historical data.
- **Backtesting** is crucial to validate a strategy before using it in real trading.
- **Challenges remain** (prediction uncertainty, confidence assessment), but machine learning offers powerful tools for trading strategies.

