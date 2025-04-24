---
uni-module: "XAI"

alias: "CART"
---

# Classification and Regression Trees

An [[Algorithmus|algorithm]] for [[Classification]] and [[Regression]] using [[Decision Tree]].

$$\hat{y}=\hat{f}(x)=\sum_{m=1}^M c_m I\left\{x \in R_m\right\}$$

- $c_m$ average of all training samples in leaf $R_m$
- minimize intra-class variances to get cutoff values
