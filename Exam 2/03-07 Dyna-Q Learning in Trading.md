## Video ID: YiKfKizPz_g
### Introduction to Dyna-Q Learning
- **Problem with Q-Learning**:
  - **Requires many experience tuples** to converge.
  - **Expensive** in trading since real trades must be executed.
- **Solution: Dyna-Q (Developed by Rich Sutton)**
  - **Builds models of T (Transition) and R (Reward)**.
  - **Hallucinates** additional experiences to update the Q-table faster.
  - Reduces reliance on real-world interactions.

## Video ID: opb7zvnlQ68
### How Dyna-Q Enhances Q-Learning
- **Q-Learning Recap**:
  1. **Initialize Q-table**.
  2. **Interact with the environment**:
     - Observe **state (S)**.
     - Execute **action (A)**.
     - Observe **new state (S')** and **reward (R)**.
     - Update **Q-table**.
  3. **Repeat many times** to improve Q-table.

- **Dyna-Q Enhancements**:
  1. **Learn models of T (transitions) and R (rewards)**.
  2. **Generate hallucinated experiences**:
     - Select **random past state-action pair**.
     - Use learned T to **simulate next state (S')**.
     - Use learned R to **simulate reward (R)**.
     - Update Q-table.
  3. **Repeat hallucinated updates 100–200 times** before interacting with real data.

- **Key Insight**:
  - **Each real-world experience is augmented with many simulated updates**.
  - **Speeds up Q-table convergence**.

## Video ID: bSY5waB4Myo
### Learning the Transition Function (T)
- **Definition of T(S, A, S')**:
  - **Probability that action A in state S leads to state S'**.
- **Building T from real experience**:
  - Maintain a **T-count table** to track transitions.
  - Each time **(S → S' given A) occurs**, increment count.
  - **Estimate probabilities** based on observed frequencies.

## Video ID: n_jiudhCSv8
### Learning the Reward Function (R)
- **Definition of R(S, A)**:
  - Expected reward for taking **action A** in **state S**.
- **Updating R using observed experience**:
  - Use a **weighted update**:
    \[
    R(s, a) \leftarrow (1 - \alpha) R(s, a) + \alpha r
    \]
  - **α (learning rate)** controls how fast the model adapts.
  - Ensures that **new experiences gradually refine the reward model**.

## Video ID: jlC0TFTUefs
### Summary of Dyna-Q Learning
- **Steps in Dyna-Q**:
  1. **Standard Q-Learning**:
     - Observe **(S, A, S', R)** from real-world experience.
     - Update **Q-table**.
  2. **Update Models of T & R**:
     - Track observed transitions **(S → S' given A)**.
     - Update **expected rewards for (S, A)**.
  3. **Hallucinate Experiences**:
     - Randomly select **(S, A)**.
     - Use T to infer **S'**, and R to infer **R**.
     - Update Q-table as if it were a real experience.
     - Repeat this process **100+ times**.
  4. **Return to real-world interaction**.

- **Why Dyna-Q is Useful**:
  - **Real-world experiences are expensive** (e.g., real trades).
  - **Hallucinated updates are cheap and improve learning speed**.

---

[Download Lecture Notes](sandbox:/mnt/data/Lecture_Dyna_Q_Learning_Trading.md)

---

Let me know if you need modifications! 🚀
