---
uni-module: "ISSP"

alias: "Inversion Lemma"
---

# Inversion Lemma (Quantiles)

Let $F$ be a [[Verteilungsfunktion|CDF]] and $p\in(0,1)$ and $t\in\mathbb{R}$.

$$F(t) \geq p \Longleftrightarrow t \geq Q_{F}^{-}(p), \quad F(t-) \leq p \Longleftrightarrow t \leq Q_{F}^{+}(p)$$

If $F$ is piecewise constant additionally:

$$F(t)>p \Longleftrightarrow t \geq Q_{F}^{+}(p), \quad F(t-)<p \Longleftrightarrow t \leq Q_{F}^{-}(p)$$

$$
\begin{aligned}
F(t) &=\sup \{p \in(0,1) \mid F(t) \geq p\}=\sup \left\{p \in(0,1) \mid t \geq Q_{F}^{-}(p)\right\} \\
F(t-) &=\inf \{p \in(0,1) \mid F(t-) \leq p\}=\inf \left\{p \in(0,1) \mid t \leq Q_{F}^{+}(p)\right\}
\end{aligned}
$$

