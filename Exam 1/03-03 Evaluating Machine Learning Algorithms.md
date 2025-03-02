# Evaluating Machine Learning Algorithms

## Video ID: xqaeZU8AD-c
### Introduction to Evaluating ML Algorithms
- **Problem**: Compare the effectiveness of different **supervised regression learning algorithms**.
- **Two Common Approaches**:
  - **Linear Regression** (Parametric Model).
  - **K-Nearest Neighbors (KNN)** (Instance-Based, Non-Parametric).
- **Goal**: Assess strengths and weaknesses of different models.

---

## Video ID: tJzbX_Pqxx4
### Understanding KNN Model Behavior
- **Example**: Query a **KNN model with K=3**.
- **Observations**:
  - The **output is piecewise constant** (i.e., step-like).
  - **No overfitting** (does not perfectly fit the data).
  - **Cannot extrapolate** beyond existing data points.

---

## Video ID: sA1K22Hmh1g
### Measuring Model Accuracy – Root Mean Squared Error (RMSE)
- **Error Calculation**:
  1. Compute the difference between **true values (Ytest)** and **predicted values (Ypredict)**.
  2. Square the differences.
  3. Take the mean.
  4. Compute the square root.

\[ RMSE = \sqrt{\frac{\sum{(Ytest - Ypredict)^2}}{N}} \]

- **Purpose**:
  - Measures **how closely the model fits the actual data**.
  - Larger errors are **penalized more** due to squaring.

---

## Video ID: MqeWkYq7958
### Out-of-Sample Testing
- **Training error alone is misleading** (a model can perfectly fit training data).
- **Out-of-sample (test) error** is more important.
- **Steps**:
  1. Train the model on the **training set**.
  2. Evaluate error on the **testing set**.

\[ RMSE_{test} > RMSE_{train} \]

---

## Video ID: yBqf9XCpz8o
### Data Splitting for Model Evaluation
- **Standard Approach**:
  - **60% Training Data**
  - **40% Testing Data**
- **Cross-Validation** (Multiple Trials):
  - Split data into **5 equal parts**.
  - Train on **80%**, test on **20%**.
  - Rotate the testing portion in each trial.

---

## Video ID: 56Nq6cs2-gc
### The Problem of Look-Ahead Bias in Finance
- **Traditional Cross-Validation** does not work well in finance.
- **Look-ahead bias**: Testing on future data while training on past data is unrealistic.
- **Solution**: **Rolling Forward Cross-Validation**
  - Train on past data → Test on future data.
  - Shift the window forward and repeat.

---

## Video ID: niXU7ISpFZA
### Correlation Between Predicted and Actual Values
- **Compare Model Output (`Ypredict`) vs. True Values (`Ytest`)**.
- **Scatter Plot**:
  - Well-aligned points → **Good model**.
  - Random scatter → **Poor model**.
- **Correlation Coefficient (`r`)**:
  - **+1.0** → Strong positive correlation.
  - **0.0** → No correlation.
  - **-1.0** → Strong negative correlation.

\[ r = corr(Ytest, Ypredict) \]

- Use **NumPy's `corrcoef()` function** to compute correlation.

---

## Video ID: mfzHchd5La8
### Overfitting in Machine Learning
- **Occurs when a model fits training data too well** but **performs poorly on test data**.
- **Example**: Polynomial models with increasing complexity.

\[ \text{Error} = f(\text{Model Complexity}) \]

- **Graph Explanation**:
  - Training error **always decreases** as complexity increases.
  - Test error **initially decreases**, but then **starts increasing** → **Overfitting Zone**.
  - **Overfitting occurs when test error rises while training error keeps dropping**.

---

### Conclusion
- **Key Evaluation Metrics**:
  - **RMSE (Root Mean Squared Error)**
  - **Out-of-Sample Testing**
  - **Cross-Validation**
  - **Correlation Analysis**
- **Avoid Overfitting**:
  - Use **rolling forward cross-validation**.
  - Monitor **test error trends**.

