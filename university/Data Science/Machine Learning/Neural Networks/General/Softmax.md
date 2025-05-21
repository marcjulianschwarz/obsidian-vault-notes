---
uni-module: AI
aliases:
  - Softmax Function
  - Normalized Exponential Function
---
# Softmax

A *smoothed* variation of the maximization function that is derivable which is important for [[Backpropagation]].

$$\sigma: \mathbb{R} \times \mathbb{R}^k \rightarrow \mathbb{R}^k$$
$$\sigma_\beta(z)_i:=\frac{e^{\beta z_i}}{\sum_{j=1}^k e^{\beta z_j}}$$
where $z=\left\langle z_1, \ldots, z_k\right\rangle, i \in\{1, \ldots, k\}$

and $e^{\beta}$ is called the base. For $\beta=1$ the function is also called the standard softmax function.

