---
uni-module: ML4ENG
---

# Lagrange Multipliers for SVM optimization

For each constraint we will use $\alpha _i$ Lagrange multipliers ([[Lagrange-Multiplikatoren]]).

$$
\begin{equation}
\mathcal{L}(\boldsymbol{w}, b, \boldsymbol{\alpha})=\frac{1}{2}\|\boldsymbol{w}\|^{2}-\sum_{i=1}^{n} \alpha_{i}\left[y_{i}\left(w \cdot x_{i}-b\right)-1\right]
\end{equation}
$$

The Lagrange multiplier needs to be maximized with $\alpha$, but we still want to minimze the whole function with $w, b$.

### Primal vs. Dual Formulation

- Primal formulation:

  $$
  \begin{equation}
  p^{*}=\min _{\boldsymbol{w}, b} \max _{\boldsymbol{\alpha}} \mathcal{L}(\boldsymbol{w}, b, \boldsymbol{\alpha})
  \end{equation}
  $$

- Dual formulation:
  $$
  \begin{equation}
  d^{*}=\max _{\boldsymbol{\alpha}} \min _{\boldsymbol{w}, b} \mathcal{L}(\boldsymbol{w}, b, \boldsymbol{\alpha})
  \end{equation}
  $$

These formulations are actually the same (Slater's condition), so we can solve the dual formulation by first minimizing the function for $w$ and $b$.

### Solution using Partial Derivatives

We would like to minimize this function:

$$
\begin{equation}
\mathcal{L}(\boldsymbol{w}, b, \boldsymbol{\alpha})=\frac{1}{2}\|\boldsymbol{w}\|^{2}-\sum_{i=1}^{n} \alpha_{i}\left[y_{i}\left(w \cdot x_{i}-b\right)-1\right]
\end{equation}
$$

To do this, we want to calculate the extreme values, so we calculate the partial derivatives for $\begin{equation} \frac{\partial \mathcal{L}}{\partial w}\end{equation}$ and $\begin{equation} \frac{\partial \mathcal{L}}{\partial b}\end{equation}$ like this:

$$
\begin{equation}
\begin{aligned}
\frac{\partial \mathcal{L}}{\partial w}=w-\sum_{i=1}^{n} \alpha_{i} y_{i} x_{i}=0 & \Rightarrow \boldsymbol{w}=\sum_{i=1}^{n} \alpha_{i} y_{i} \boldsymbol{x}_{i} \\
\frac{\partial \mathcal{L}}{\partial b}=-\sum_{i=1}^{n} \alpha_{i} y_{i} &=0 \Rightarrow \sum_{i=1}^{n} \alpha_{i} y_{i}=0
\end{aligned}
\end{equation}
$$

We then insert the results for $w$ and $b$ resulting in the reamining maximization problem under two constraints.

$$
\begin{equation}
\mathcal{L}(\boldsymbol{w}, b, \boldsymbol{\alpha})=\sum_{i=1}^{n} \alpha_{i}-\frac{1}{2} \sum_{i, j=1}^{n} y_{i} y_{j} \alpha_{i} \alpha_{j}\left(\boldsymbol{x}_{i} \cdot \boldsymbol{x}_{j}\right)
\end{equation}
$$

This is the optimization problem now:

$$
\begin{equation}
\begin{gathered}
\max _{\boldsymbol{\alpha}} \mathcal{L}(\boldsymbol{w}, b, \boldsymbol{\alpha}) \\
\text { s.t. } \alpha_{i} \geq 0, \sum_{i=1}^{n} \alpha_{i} y_{i}=0
\end{gathered}
\end{equation}
$$

also see [[Karush-Kuhn-Tucker Conditions]].
