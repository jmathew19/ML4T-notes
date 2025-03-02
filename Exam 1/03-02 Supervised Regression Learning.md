# Supervised Regression Learning

## Video ID: _CznJ6phPsg
### Introduction to Supervised Regression Learning
- **Regression** = Using data to **build a model** that predicts a **numerical output** based on numerical inputs.
- Alternative term: **Numerical Model** (but "regression" is commonly used).

---

## Video ID: 6EC1w_fs5u8
### Parametric Regression (Model-Based Approach)
- **Example Problem**: Predict rainfall based on **barometric pressure changes**.
- **Data Representation**:
  - X = Change in barometric pressure.
  - Y = Amount of rainfall.
  - **Scatter plot** shows a trend: **decreasing pressure → increased rainfall**.
- **Linear Regression Model**:
  \[ y = m x + b \]
  - **m, b** = Parameters of the model.
  - Given a new **x** (pressure change), we **predict y** (rainfall) using this equation.
- **Polynomial Regression**:
  \[ y = m_2 x^2 + m x + b \]
  - **More parameters (m2, m, b)** to improve accuracy.
  - **Higher-order terms** fit complex data patterns.
- **Parametric Model Characteristic**:  
  - **Learns model parameters**.
  - **Discards training data after learning**.

---

## Video ID: CWCLQ6eu2Do
### Instance-Based Learning (Non-Parametric)
- **Keeps the training data** instead of just storing model parameters.
- **Example**: Predict rainfall based on past data (KNN approach).
  - Given **X = -5 mm pressure change**, find **3 nearest historical data points (K=3)**.
  - Compute **mean Y** of these nearest values as the prediction.

---

## Video ID: ZhJTGBbR18o
### K-Nearest Neighbors (KNN) vs. Kernel Regression
- **KNN**:
  - Finds the **K-nearest data points** and averages their Y-values.
  - Each neighbor contributes **equally** to the prediction.

- **Kernel Regression**:
  - **Weights neighbors** based on **distance** (closer points have more influence).

- **Comparison of Parametric vs. Non-Parametric Methods**:
  - **Parametric** → Learns a formula (e.g., **y = mx + b**).
  - **Non-Parametric** → Stores data and uses it at query time.

---

## Video ID: P2NqrFp8usY
### Training and Testing Machine Learning Models
- **Stock Price Prediction Example**:
  - **X** = Stock indicators (e.g., Bollinger Bands, momentum).
  - **Y** = Future price.

- **Data Splitting for Model Evaluation**:
  - **Training Set (X_train, Y_train)** → Used to **train the model**.
  - **Testing Set (X_test, Y_test)** → Used to **evaluate the model**.

- **Out-of-Sample Testing**:
  - **Essential** to prevent overfitting.
  - **Train on past data, test on future data** (not the reverse).

---

## Video ID: -roGBKfEXog
### Standardized API for Machine Learning Models
- **Consistency in model implementation** allows easy comparison.
- **Standard API includes**:
  1. **Constructor** → Creates model instance.
  2. **Train Method** → Learns from `X_train`, `Y_train`.
  3. **Query Method** → Predicts `Y` given `X_test`.

**Example API for Linear Regression Learner**:
```python
class LinRegLearner:
    def __init__(self):
        pass

    def train(self, X, Y):
        self.m, self.b = some_regression_library(X, Y)

    def query(self, X):
        return X * self.m + self.b
```
- **KNNLearner API follows the same structure**, but with an added **K parameter**.

---

## Video ID: nsol5aKIbF8
### Implementing Linear Regression in Python (Pseudo Code)
```python
class LinRegLearner:
    def __init__(self):
        pass  # No initialization needed for linear regression

    def train(self, X, Y):
        self.m, self.b = perform_linear_regression(X, Y)  # Finds best m, b

    def query(self, X):
        return X * self.m + self.b  # Predicts Y for given X
```
- **Train Method**:
  - Uses **SciPy/NumPy** to compute **m, b**.
- **Query Method**:
  - Applies the equation \( y = m x + b \) to make predictions.

---

### Conclusion
- **Parametric Learning**: Stores **model parameters** (linear/polynomial regression).
- **Instance-Based Learning**: Stores **data** (KNN, Kernel Regression).
- **Model Evaluation**: Use **out-of-sample testing** to measure accuracy.
- **Standardized API**: Helps compare different machine learning techniques.

