

## **Introduction to Optimizers**
- **Optimizers** are algorithms used to:
  - Find the minimum values of functions.
  - Determine parameters for models using data.
  - Optimize stock allocations in portfolios.

### **Steps to Use an Optimizer**
1. Define the function to minimize.
   - Example: `f(x) = x^2 + 0.5`
2. Provide an initial guess.
   - If unsure, use a random or standard value.
3. Call the optimizer and let it iterate to find the minimum.

---

## **Gradient Descent & Function Minimization**
- Example: `f(x) = (x - 1.5)^2 + 0.5`
  - **Gradient Descent**: Algorithm moves in the direction of the steepest decrease.
  - Uses **derivatives** to iteratively update `x` towards the minimum value.
- **SciPy Library**
  - SciPy provides different minimization methods.
  - Example usage in Python:
    ```python
    import scipy.optimize as spo
    result = spo.minimize(f, x_guess, method='SLSQP', options={'disp': True})
    ```

---

## **Convex vs. Non-Convex Optimization Problems**
- **Convex Functions**:
  - A function is convex if the line segment between any two points lies **above** the graph.
  - They have **one** global minimum.
  - Optimizers efficiently find the solution.
- **Non-Convex Functions**:
  - May contain multiple local minima.
  - Harder for optimizers to find the global minimum.
  - Require more advanced techniques.
- Optimizers work well in **multiple dimensions** (e.g., multi-variable functions).

---

## **Using Optimizers for Model Fitting**
### **Parameterized Models**
- Example: Linear Model `y = mx + b`
  - `m` (slope) and `b` (intercept) are parameters.
  - We fit a model by finding the best `m` and `b`.
- Given **experimental data**, we use an optimizer to find parameters that best fit the data.

### **Error Minimization Approach**
1. Define an **error function** measuring the difference between actual and predicted values.
   - Example: **Squared Error**
     ```python
     error = sum((actual - predicted)^2)
     ```
2. Use an optimizer to minimize this error.
3. Adjust parameters iteratively until the best fit is found.

### **Implementation in Python**
```python
import numpy as np
import scipy.optimize as spo

def error(params, data):
    C0, C1 = params
    x, y_actual = data
    y_pred = C0 * x + C1
    return np.sum((y_actual - y_pred) ** 2)

data = (np.array([1,2,3]), np.array([2.1, 2.9, 3.9]))  # Sample data
initial_guess = [1, 1]  # Initial values for slope and intercept
result = spo.minimize(error, initial_guess, args=(data,), method='SLSQP')
```

---

## **Polynomial Model Fitting**
- Just like linear models, we can fit **higher-degree polynomials** to data.
- **Generalized function:**
  ```python
  y = C0 * x^4 + C1 * x^3 + C2 * x^2 + C3 * x + C4
  ```
- Uses the same minimization process with additional coefficients.

### **Example Output**
- Original polynomial: `1.5x^4 - 10x^3 - 5x^2 + 3x + 7`
- Optimized coefficients: `1.6, -10.5, -5.1, 3.2, 7.3`
- Produces a model that closely fits the data despite noise.

---

## **Portfolio Optimization**
### **Definition**
- **Portfolio Optimization**: Finding the best allocation of funds across assets to **maximize performance**.
- Performance criteria:
  - **Cumulative Return**
  - **Volatility (Risk)**
  - **Sharpe Ratio** (Risk-adjusted return)

### **Example Portfolio**
- Assets: Google, Apple, Gold, Exxon
- **Equal Allocation (Unoptimized Portfolio)**
  - 25% allocated to each asset.
- **Optimized Portfolio (Maximized Sharpe Ratio)**
  - Example result: 60% Gold, 40% Apple, 0% Google/Exxon
  - Yields better performance than S&P 500 benchmark.

### **Optimization Process**
1. **Define an objective function** to optimize.
   - Sharpe Ratio is typically maximized.
2. **Use an optimizer** to find the best allocation.
   - Allocations are adjusted iteratively to maximize performance.
3. **Apply constraints**:
   - Sum of allocations must equal 100%.
   - No short-selling (allocations must be between 0 and 1).

---

## **Mathematical Formulation of Sharpe Ratio Optimization**
- **Sharpe Ratio Formula**:
  ```
  Sharpe Ratio = (Mean Portfolio Return - Risk-Free Rate) / Portfolio Volatility
  ```
- **Optimization Step**:
  - Instead of **maximizing** Sharpe Ratio, we **minimize its negative**:
    ```python
    objective = -Sharpe Ratio
    ```

### **Constraints for Optimization**
1. **Bound Constraints**: Allocation values must be between 0 and 1.
2. **Sum Constraint**: Total allocation must sum to 100%.

### **Python Implementation**
```python
from scipy.optimize import minimize

def sharpe_ratio(weights, returns, risk_free_rate=0):
    portfolio_return = np.sum(weights * returns.mean())
    portfolio_volatility = np.sqrt(np.dot(weights.T, np.dot(returns.cov(), weights)))
    return -(portfolio_return - risk_free_rate) / portfolio_volatility

def optimize_portfolio(returns):
    num_assets = returns.shape[1]
    initial_guess = [1./num_assets] * num_assets  # Equal weight
    bounds = [(0, 1) for _ in range(num_assets)]
    constraints = ({'type': 'eq', 'fun': lambda x: np.sum(x) - 1})
    result = minimize(sharpe_ratio, initial_guess, args=(returns,), bounds=bounds, constraints=constraints)
    return result.x  # Optimized allocations
```

---

## **Conclusion**
- **Optimization is a powerful tool** used in function minimization, model fitting, and portfolio management.
- **Gradient descent** is a fundamental technique used in many optimization problems.
- **Convex problems** are easier to solve, but optimizers can handle non-convex problems with some difficulty.
- **Portfolio Optimization**:
  - Uses **minimization** to maximize **Sharpe Ratio**.
  - Constraints ensure feasible allocations.
  - Optimized portfolios often outperform naive equal-weight portfolios.

### **Next Steps**
- Experiment with different **minimization methods** in SciPy.
- Try optimizing for different portfolio performance metrics.
- Explore advanced **machine learning optimizers** for financial data.

