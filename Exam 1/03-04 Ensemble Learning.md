# Ensemble Learning

## Video ID: OKGBfCewE5g
### Introduction to Ensemble Learning
- In 1988, **Michael Kearns and Leslie Valiant** posed the question:  
  **Can weak learners be combined into a strong learner?**
- **Example: Netflix Prize (2006-2009)**:
  - Netflix offered a **$1 million prize** for an algorithm **10% better** than their existing recommendation system.
  - The **winning solution** was **not a single model**, but an **ensemble of models**.
  - This demonstrated the **power of ensemble methods**.

---

## Video ID: Un9zObFjBH0
### What is an Ensemble Learner?
- **Not a new algorithm**, but a **combination of multiple models**.
- Example:  
  - Instead of just using **KNN**, also use:
    - **Linear Regression**
    - **Decision Trees**
    - **Support Vector Machines (SVMs)**
- **Querying an ensemble**:
  1. Pass **X** to each model.
  2. Each model **predicts Y**.
  3. **Combine predictions** (e.g., take the **mean** for regression).
- **Why use ensembles?**
  - **Lower error** compared to a single model.
  - **Less overfitting**.
  - **Reduces model bias** by combining different learning perspectives.

---

## Video ID: 2Mg8QD0F1dQ
### Bagging (Bootstrap Aggregating)
- Introduced by **Leo Breiman** in the 1990s.
- Instead of using different models, **train the same model** on **different subsets** of data.
- **Steps in Bagging**:
  1. Randomly sample **N'** points **with replacement** from the full dataset (**N**).
  2. Repeat this **M times** to create **M bags of data**.
  3. Train **M models** on these different datasets.
  4. Predict using all models and **average their predictions**.
- **Rule of Thumb**:  
  - **N' ≈ 60% of N** (each subset contains ~60% of the full data).

---

## Video ID: sVriC_Ys2cw
### Visualizing Bagging with KNN
- Example: Create **multiple 1-nearest neighbor (1-NN) models** using bagging.
- Each model:
  - **Overfits individually**.
  - But when combined, the **ensemble smooths out the noise**.
- **Ensemble result**:
  - Averages multiple KNN models.
  - **Reduces overfitting**.
  - **Improves generalization**.

---

## Video ID: GM3CDQfQ4sw
### Boosting (Adaptive Weighting)
- **Boosting** improves upon bagging by **focusing on mistakes**.
- **AdaBoost (Adaptive Boosting) Algorithm**:
  1. Train a model on a random subset.
  2. Identify **poorly predicted data points**.
  3. Give **higher weight** to misclassified points.
  4. Train the next model **with priority on difficult cases**.
  5. Repeat this process **M times**.
- **Difference from Bagging**:
  - **Bagging**: Samples **randomly**.
  - **Boosting**: Samples **based on past errors**.

---

## Video ID: INtcc3icJTo
### Summary of Ensemble Learning
- **Bagging & Boosting are NOT new models**.
- They are **meta-algorithms** that **wrap around existing models**.
- **Advantages**:
  - **Reduces overfitting**.
  - **Improves prediction accuracy**.
  - **Works with any learner (KNN, Linear Regression, Decision Trees, etc.)**.
- **Use the same API** for an ensemble as you would for a single model.

---

### Conclusion
- **Bagging**: Improves models by training on **random data subsets**.
- **Boosting**: Focuses on **hard-to-learn** data points.
- **Ensembles** are widely used in **machine learning for trading** and other applications.

