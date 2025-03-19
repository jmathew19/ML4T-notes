
## Video ID: DHddueClCg0
### Introduction to Portfolio Optimization
- **Key Question**: How should we allocate investments among stocks?
- **Mean-Variance Optimization (MVO)**:
  - Helps determine asset allocation to **minimize risk** for a **given return target**.
- **Goal**: Find the best mix of equities that reduces risk while achieving the desired return.

## Video ID: 3C0OpFT-Vlg
### Defining Risk: Volatility as Standard Deviation
- **Risk = Volatility**:![[Screenshot 2025-03-19 at 5.10.20 PM.png]]
  - Measured as **standard deviation of daily returns**.
- **Example**:
  - **Stock XYZ**: 10% return, but high volatility.
  - **Stock ABC**: 10% return, lower volatility.
  - Lower volatility is **preferred for minimizing risk**.

## Video ID: 7SxSmJTrKXE
### Risk-Return Tradeoff in Portfolio Construction![[Screenshot 2025-03-19 at 5.13.05 PM.png]]
- **Scatter Plot Representation**:
  - **X-axis**: Risk (Volatility).
  - **Y-axis**: Return.
  - **Each dot represents a stock**.
- **Portfolio Construction**:
  - By combining stocks, a **portfolio has intermediate risk and return**.
  - Goal: **Optimize stock mix to balance risk and return**.

## Video ID: 7boCbpchurA
### Markowitz’s Insight: The Role of Covariance
- **Traditional Approach**:
  - Investors equally weighted assets or picked stocks based on individual returns.
- **Harry Markowitz’s Contribution**:
  - Discovered that **covariance between stocks** affects portfolio risk.
  - **Low correlation (or negative correlation) reduces total risk**.
  - **Blending assets wisely can achieve lower risk than any single asset**.
- **Key Finding**:
  - **A mix of stocks and bonds can be lower risk than either asset alone**.

## Video ID: qOl04hw7f9g
### Understanding Covariance in Portfolio Construction
- **Three Sample Stocks**:![[Screenshot 2025-03-19 at 5.19.34 PM.png]]
  - **ABC & DEF**: **Move together** (correlation = **0.9**).
  - **GHI**: **Moves opposite** to ABC & DEF (**negative correlation**).
  - 0.9 mean very close together 
  - -0.9 means low correlation 
- **Portfolio Experiments**:
- **Experiment 1**: ABC + DEF (High Correlation)→ No risk reduction.
	- ![[Screenshot 2025-03-19 at 5.22.55 PM.png]]
	- no real advantage since port has the same volatility as the others stocks indiviually
- **Experiment 2**  ABC + DEF + GHI (Negative Correlation) → **Lower volatility, same return**.
	- ![[Screenshot 2025-03-19 at 5.24.37 PM.png]]
	  This allocation has also a 10% return as the other, but this graph is smother
	- Same return with less volatility 
- **Key Insight**:
  - **Combining negatively correlated assets reduces portfolio volatility**.
  - **Diversification benefits arise from assets that don't move in lockstep**.

## Video ID: RoUZKkRenRo
### The Power of Mean-Variance Optimization
- **Markowitz’s Key Realization**:
  - **Variance & covariance matter more than individual risk**.
  - **Combining uncorrelated or negatively correlated assets lowers overall portfolio risk**.
- **Mean-Variance Optimization (MVO)**:
  - Finds the **best mix of assets** by analyzing: 
	  - Input
		- **Expected return** (predicted performance).
		- **Volatility** (historical risk).
	    - **Covariance matrix** (relationship between assets).
	    - **Target Return** (Goal return)
    - Output:
	    - Asset weights for portfolio that minimizes risk
![[Screenshot 2025-03-19 at 5.32.15 PM.png]]
### How Portfolio Optimizers Work
- **Inputs for Portfolio Optimization**:
  1. **Expected Return** (future estimated gains).
  2. **Volatility** (historical fluctuations).
  3. **Covariance Matrix** (relationship between assets).
  4. **Target Return** (desired return level).
- **Optimizer Output**:
  - **Optimal weights for each stock** that **minimize risk while achieving the target return**.

## Video ID: vnAbsNN3SbA
### The Efficient Frontier
![[Screenshot 2025-03-19 at 5.36.35 PM.png]]
- **Defining the Efficient Frontier**:
  - **For a given return, what is the minimum risk?**
  - **For a given risk, what is the maximum return?**
- **Efficient Portfolios**:
  - Portfolios **on the efficient frontier** are **optimal**.
  - Portfolios **inside the frontier** are **suboptimal** (higher risk, lower return).
- **Key Takeaways**:
  - Investors **should aim for portfolios on the efficient frontier**.
  - The **tangent line to the efficient frontier** represents the **maximum Sharpe ratio portfolio**.
![[Screenshot 2025-03-19 at 5.37.05 PM.png]]

## Video ID: vnAbsNN3SbA
### Practical Considerations in Portfolio Optimization
- **Key Lessons from Modern Portfolio Theory**:
  1. **More diversification reduces risk**.
  2. **Optimal portfolios minimize volatility through low-correlated assets**.
  3. **The efficient frontier defines the best possible return for a given risk level**.
