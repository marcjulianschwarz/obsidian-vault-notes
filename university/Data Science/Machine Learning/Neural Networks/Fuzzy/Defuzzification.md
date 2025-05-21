---
uni-module: MBNN
---
# Defuzzification

$$out(x)=\sum_{k=1}^R \frac{\kappa_k b_k(x)}{\sum_{l=1}^R \kappa_l b_l(x)} w_k$$
with $R$ the number of rules and $\kappa$ the belief factors
$$\sum_{k=1}^R \kappa_k=1 \quad \kappa_k>0.$$

