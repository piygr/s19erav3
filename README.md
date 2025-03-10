# **GridWorld Value Iteration using Bellman Equation**

## **📌 Problem Statement**
We have a **4x4 GridWorld**, where an agent starts at the **top-left corner (state 0)** and tries to reach the **bottom-right corner (state 15)**. The agent can move **up, down, left, or right** with equal probability. The rewards are:
- **-1 for each move**
- **0 for reaching the terminal state (bottom-right corner)**

We apply **Value Iteration** using the **Bellman equation**:

\[
V(s) = \sum_{s'} P(s'|s,a) [R + \gamma V(s')]
\]

where:
- \( P(s'|s,a) \) is the transition probability (equal for all actions)
- \( R \) is the reward per move (-1)
- \( \gamma \) (gamma) is the discount factor (set to **1** for no discounting)
- We **stop when the maximum change** in \( V(s) \) across all states is **< 1e-4**

---

## **✅ Output**
```
[[-59.42367735 -57.42387125 -54.2813141  -51.71012579]
 [-57.42387125 -54.56699476 -49.71029394 -45.13926711]
 [-54.2813141  -49.71029394 -40.85391609 -29.99766609]
 [-51.71012579 -45.13926711 -29.99766609   0.        ]]
```
