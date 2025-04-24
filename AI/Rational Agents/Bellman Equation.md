---
uni-module: AI
---
# Bellman Equation

$$U(s)=R(s)+\gamma \cdot \max _{a \in A(s)} \sum_{s^{\prime}} U\left(s^{\prime}\right) \cdot P\left(s^{\prime} \mid s, a\right)$$

In other words:

The utility in state $s$ is the current reward in state $s$ plus $\gamma$ times the expected reward of the best possible action. 