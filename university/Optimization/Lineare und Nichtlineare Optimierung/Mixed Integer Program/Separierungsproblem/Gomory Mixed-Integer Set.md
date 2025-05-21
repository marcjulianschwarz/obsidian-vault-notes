---
uni-module: "LNS"
---

# Gomory Mixed-Integer Set

$$X^{G O M}=\left\{\left(y_{0}, y, x\right) \in \mathbb{Z}^{1} \times \mathbb{Z}_{+}^{p} \times \mathbb{R}_{+}^{q}: y_{0}+\sum_{j} a_{j} y_{j}+\sum_{k} g_{k} x_{k}=b\right\}$$

mit $b\notin\mathbb{Z}^1$.

Umformung in [[Continous Integer Knapsack Set]]:
$$\left\{\left(y_{0}, y, s\right) \in \mathbb{Z}^{1} \times \mathbb{Z}_{+}^{p} \times \mathbb{R}_{+}^{1}: y_{0}+\sum_{j} a_{j} y_{j} \leq b+s\right\}$$

mit [[Mixed Integer Rounding Ungleichung|MIR]] Ungleichung:

$$y_{0}+\sum_{j}\left(\left\lfloor a_{j}\right\rfloor+\frac{\left(f_{j}-f_{b}\right)^{+}}{1-f_{b}}\right) y_{j} \leq\lfloor b\rfloor-\sum_{k: g_{k}<0} \frac{g_{k}}{1-f_{b}} x_{k} .$$
→ [[Gomory Mixed-Integer Ungleichung]]
