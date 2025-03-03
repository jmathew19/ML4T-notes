# Stock Trading Mechanics and Market Exploits

## **Introduction to Stock Trading**
- When trading stocks online (e.g., E-Trade, Interactive Brokers), there is a complex underlying system handling the transaction.
- The process involves **orders**, **brokers**, **exchanges**, and **order execution mechanisms**.

---

## **Types of Orders**

![[Screenshot 2025-03-01 at 10.45.09 PM.png]]
### **1. Market Order**
- Buys or sells a stock **immediately** at the **best available price**.
- Execution is guaranteed, but the price **may fluctuate**.
- Example:
  ```
  Buy 150 shares of Google, market
  ```

### **2. Limit Order**
- Specifies the **maximum price** (for buying) or **minimum price** (for selling).
- Execution is **not guaranteed**; the price must reach the limit for the order to complete.
- Example:
  ```
  Buy 100 shares of IBM, limit 99.95
  ```
  - This order will **only execute if** IBM’s stock price is **$99.95 or lower**.

---

## **Order Book Mechanics**
- Every exchange maintains an **order book** for each stock.
- **Bids**: Orders to buy at a specific price.
- **Asks**: Orders to sell at a specific price.
- Example Order Book:
  ```
  Bids:
  - 100 shares @ $99.95
  - 500 shares @ $99.90
  - 200 shares @ $99.85
  
  Asks:
  - 1,000 shares @ $100.00
  - 600 shares @ $100.05
  - 300 shares @ $100.10
  ```
- When a **market buy order** is placed, it is executed at the **lowest available ask price**.
- When a **market sell order** is placed, it is executed at the **highest available bid price**.


![[Screenshot 2025-03-01 at 10.48.17 PM.png]]
![[Screenshot 2025-03-01 at 10.49.15 PM.png]]
---

## **Order Execution and Broker Role**
### **How Orders Reach the Market**
1. You enter an order on your **broker’s platform**.
2. The broker routes it to **various exchanges** (NYSE, NASDAQ, BATS, etc.).
3. The broker selects the best exchange based on **price and liquidity**.
4. The order is executed, and the confirmation is sent back to you.

### **Internal Execution and Dark Pools**
- Sometimes, brokers execute orders **internally** without going to an exchange.
- Brokers can also use **Dark Pools**, private trading venues where large transactions occur anonymously.
- **80-90% of retail orders never reach public exchanges**, reducing **market impact and fees**
- **Broker to exchange:**![[Screenshot 2025-03-01 at 10.51.27 PM.png]]
- Intra broker exchange
	- ![[Screenshot 2025-03-01 at 10.52.41 PM.png]]
- Inter broker exchange
	- ![[Screenshot 2025-03-01 at 10.53.27 PM.png]]


---

## **High-Frequency Trading (HFT) Exploits**
### **1. Order Book Exploit**
- **Colocated hedge fund computers** are positioned near exchanges.
- They receive order book updates **milliseconds before** remote traders.
- The hedge fund can:
  - Detect buying pressure.
  - **Buy shares ahead of retail investors**.
  - Sell them **at a higher price** when the retail order arrives.
![[Screenshot 2025-03-01 at 10.54.16 PM.png]]


### **2. Geographic Arbitrage**
- Prices **slightly differ** across geographically separated exchanges (e.g., NYSE vs. London Stock Exchange).
- Hedge funds with **high-speed connections** between exchanges can:
  - Buy stock where the price is lower.
  - Sell stock where the price is higher.
  - Capture risk-free **arbitrage profits**.

![[Screenshot 2025-03-01 at 10.54.32 PM.png]]


---

## **Advanced Order Types** 
Implemented by brokers
### **1. Stop Loss Order**
- Automatically sells when a stock drops to a specified price.
- Example:
  ```
  Stop loss: Sell 100 shares of AAPL if price drops below $120
  ```
- Protects against **big losses**.

### **2. Stop Gain (Take Profit) Order**
- Automatically sells when a stock **rises to a target price**.
- Locks in profits.

### **3. Trailing Stop Order**
- A **dynamic stop loss** that moves **as the stock price increases**.
- Example:
  ```
  Sell if price drops 5% from the highest price reached
  ```
- Protects gains **while allowing potential profit growth**.

### **4. Short Selling**
- Profiting from **falling stock prices**.
- You **borrow shares**, sell them, and later **buy them back at a lower price**.

![[Screenshot 2025-03-01 at 10.56.13 PM.png]]
![[Screenshot 2025-03-01 at 10.57.03 PM.png]]

---

## **Short Selling Mechanics**
### **Step 1: Borrow Shares**
- You borrow **100 IBM shares** (currently at $100 each) from another investor.

### **Step 2: Sell Immediately**
- You sell the borrowed shares to a buyer for **$10,000 (100 × $100)**.

### **Step 3: Buy Back Later (Covering the Short)**
- If IBM stock **drops to $90**, you buy **100 shares** for **$9,000**.
- You return the shares to the lender and **keep the $1,000 profit**.

### **What Can Go Wrong?**
- If IBM **rises to $150**, you must buy back **at a loss**.
- Instead of a profit, you **lose $5,000 ($15,000 – $10,000)**.
- **Short selling has unlimited risk** (a stock can rise indefinitely).

---

## **Conclusion**
- **Market Orders vs. Limit Orders**: Market orders execute immediately; limit orders wait for target prices.
- **Order Book**: Tracks supply and demand in real-time.
- **High-Frequency Trading**: Hedge funds exploit latency and price differences.
- **Advanced Order Types**: Stop loss, stop gain, trailing stop, and short selling strategies.
- **Short Selling Risks**: Potential for unlimited losses if prices rise.

### **Next Steps**
- Study **portfolio optimization** techniques.
- Explore **algorithmic trading strategies**.
- Learn how **machine learning** is applied in financial markets.

