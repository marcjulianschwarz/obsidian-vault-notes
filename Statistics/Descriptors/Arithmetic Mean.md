---
uni-module: "ISSP"

alias: ["Mean", "Durchschnitt", "Arithmetisches Mittel", "Mittel"]
---

# Arithmetic Mean

$$M(t)=\frac{1}{n} \sum_{k=1}^n t_k$$

**Properties**
If we have $\mathbb{E}\left(X_1^2\right)<\infty$ , then for the [[Arithmetic Mean]] $\bar{X}_{(n)}$ we have:
$$\mathbb{E}\left(\bar{X}_{(n)}\right)=\mu, \quad \mathbb{V}\left(\bar{X}_{(n)}\right)=\frac{\sigma^2}{n}$$
_Of course the [[Erwartungswert|Expectation]] is $\mu$ as this is exactly what we want to estimate with the arithmetic mean estimator._

Given the [[Zentraler Grenzwertsatz|Central Limit Theorem]] the [[Wahrscheinlichkeitsmaß|Distribution]] of the [[Arithmetic Mean]] is for large $n$ in good approximation a [[Normalverteilung|Normal Distribution]] with:

$$N\left(\mathbb{E}\left(\bar{X}_{(n)}\right), \mathbb{V}\left(\bar{X}_{(n)}\right)\right)=N\left(\mu, \sigma^2 / n\right)$$

[[stochastisch unabhängig|independent]] of the particular distribution of $X_1$.
