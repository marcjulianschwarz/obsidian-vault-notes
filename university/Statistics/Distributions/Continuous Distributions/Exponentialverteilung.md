---
uni-module: "StochMod"

alias: "Exponential Distribution"
---

# Exponentialverteilung

Für $\alpha > 0$:
$$f(x):=\alpha e^{-\alpha x} \mathbb{1}_{[0, \infty)}(x), \quad x \in \mathbb{R}$$
wir schreiben auch:
$$Exp(\alpha)$$
[[Verteilungsfunktion|CDF]]:
$$F(x)= \begin{cases}0, & x \leq 0 \\ 1-e^{-\alpha x}, & x>0\end{cases}$$
