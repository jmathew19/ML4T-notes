# Technical Analysis in Trading

## Video ID: wnCd7JdGWZc
### Two Main Approaches in Stock Selection:
1. **Fundamental Analysis**:  
   - Evaluates a company's financial health (earnings, cash flow, book value, etc.).  
   - Investors seek stocks priced below their **intrinsic value**.

2. **Technical Analysis** (Focus of this lesson):  
   - **Ignores company fundamentals**.  
   - Uses **historical price and volume** to identify patterns and trends.  
   - Traders look for signals based on past price movements.

---

## Video ID: 8cv8qp9CDj0
### Characteristics of Technical Analysis
- **Focuses only on price and volume** (no earnings, dividends, etc.).
- Uses **historical data** to compute **indicators**.
- **Indicators**: Statistical signals that hint at **buying or selling opportunities**.

### Criticism of Technical Analysis
- Some argue it’s not valid because it ignores fundamental value.
- **Support for Technical Analysis**:
  - Prices **reflect market sentiment**.
  - **Heuristics work in AI**, and similar logic applies to price trends.
  - Price deviations from the market might indicate **opportunities**.

---

## Video ID: 153ab3FwNhk
### Effectiveness of Technical Analysis
- **Individual indicators are weakly predictive** (useful in the 80s & 90s, less so now).
- **Combining multiple indicators enhances prediction power**.
- **Look for contrasts**:
  - Stocks moving **differently from the market** could be signals.
- Works **better over short time periods** than long-term investing.

---

## Video ID: 3_k0eoIKNj8
### Trading Horizon and Analysis Type
| Time Horizon  | Best Analysis Type  |
|--------------|------------------|
| **Milliseconds** | **Technical Analysis** (Order book, momentum) |
| **Days** | **Combination of Both** |
| **Years** | **Fundamental Analysis** (Earnings, long-term value) |

- **Computers** excel at **high-speed, simple decisions** (high-frequency trading).  
- **Humans** excel at **long-term, complex investment choices**.  
- **Middle ground** = Humans + AI collaboration.

---

## Video ID: H7_J3jfiS5I
### Key Technical Indicators
1. **Momentum** (measures trend strength).
2. **Simple Moving Average (SMA)** (smooths price fluctuations).
3. **Bollinger Bands** (measures volatility).

---

## Video ID: 4eKsY-KXEnc
### 1. Momentum Indicator
- **Measures price movement strength** over `n` days.
- Formula:  
  \[ Momentum(t) = \frac{Price_t}{Price_{t-n}} - 1 \]
- Interpretation:
  - **Positive momentum** → Strong **uptrend**.
  - **Negative momentum** → Strong **downtrend**.
- Used by traders to **identify trends early**.

---

## Video ID: 4eKsY-KXEnc
### 2. Simple Moving Average (SMA)
- **Averages past prices over `n` days** to smooth volatility.
- Formula:  
  \[ SMA_t = \frac{1}{n} \sum_{i=t-n}^{t} Price_i \]
- **Uses:**
  1. **Trend Confirmation**: Price crossing SMA can signal **buy/sell points**.
  2. **Mean Reversion**: Large deviations from SMA indicate **overbought/oversold conditions**.

---

## Video ID: z63Cxk0bUOQ
### 3. Bollinger Bands
- **Expands and contracts based on volatility**.
- Formula:  
  \[ Bollinger\ Band(t) = \frac{Price_t - SMA_t}{2 	imes \sigma} \]
  - \( \sigma \) = Standard deviation of past `n` days.

**How Traders Use Bollinger Bands:**
- **Buy Signal**: Price moves below **lower band** and crosses **back inside**.
- **Sell Signal**: Price moves above **upper band** and crosses **back inside**.

---

## Video ID: sDu6CudKa0Q
### Normalization in Technical Indicators
- Different indicators operate on **different scales**.
- **Issue**: Some indicators dominate over others (e.g., PE ratio vs. Bollinger Bands).
- **Solution**: Normalize all indicators to the same scale:
  \[ Normalized\ Value = \frac{X - mean(X)}{std(X)} \]
- Ensures **fair weighting** when combining indicators.

---

## Video ID: ZQu3GO5Rdik
### Summary of Technical Analysis
- **Indicators are heuristics** that help traders spot **price trends**.
- Combining multiple indicators **improves accuracy**.
- **Normalization is essential** when using multiple indicators.
- **Technical analysis works best in short-term trading**, not long-term investing.

---

### Next Lesson Preview:
- Introduction to **historical price and volume data** for computational trading.
