---
uni-module: "PR"

alias: ["Sigmoid Function", "Logistic Sigmoid Function"]
---

# Logistic Function

The logistic function which is defined in $[0,1]$ looks like this

$$L(x)=\frac{1}{1+e^{-F(x)}}$$
$$f(x)=\frac{1}{1+e^{-x}}$$

In a [[Classification]] task the function $F(x)$ is also called the [[Decision Boundary]].

One interesting property of the logistic function is its **derivative:**
$$g(x)(1-g(x))$$
This derivative is useful as we need it to compute the [[Gradient Descent]] update rules. 

By adding a coefficient $a$ to the $x$ we can rearange probabilites of class membership.
