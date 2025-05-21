---
uni-module: AI
aliases:
  - Normalization
---
# Probability Normalization

We can use this if we have $P(A\land B)$ and we want to know $P(B)$. Or just in general when we want to compute a [[Posterior Probability|Conditional Probability]].

$$P(A\mid B)=\alpha P(A\land B)$$
In the end we just have to scale the sum of the relative probabilities to equal $1$ with the normalization constant $\alpha$.

