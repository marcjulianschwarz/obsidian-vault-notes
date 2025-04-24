---
uni-module: "XAI"

alias: "GAM"
---

# Generalized Additive Model

Similar to [[Generalized Linear Model|GLM]] but we allow any weight function (can be nonlinear too)
$$g\left(E_Y(y \mid x)\right)=\beta_0+f_1\left(x_1\right)+f_2\left(x_2\right)+\ldots+f_p\left(x_p\right)$$

So we add a set of basis functions for each feature as new features.

- [[Spline]]
- [[Radial Basis Function Kernel]]
- Shifted [[Logistic Function|Sigmoid Function]]
