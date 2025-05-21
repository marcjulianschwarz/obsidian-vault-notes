---
uni-module: "ISSP"
---

# Standard Estimators

- [[Arithmetic Mean]]
- [[Varianz|Variance]] [[Sample Variance]]
- [[Empirical cumulative distribution functions|ECDF]]

You can use these estimators to estimate the [[Erwartungswert|Expectation]] , [[Varianz|Variance]] and [[Verteilungsfunktion|CDF]] of an n-fold experiment:

Estimate [[Erwartungswert|Expectation]]:
$$\bar{X}_{(n)}: \mu=\mathbb{E}\left(X_{1}\right), \sigma_{n}^{2}=\mathbb{V}\left(X_{1}\right) / n, \text { if } \mathbb{E}\left(X_{1}^{2}\right)<\infty$$
Estimate [[Varianz|Variance]]:
$$S_{(n)}^{2}: \mu=\mathbb{V}\left(X_{1}\right), n \sigma_{n}^{2} \rightarrow \mathbb{V}\left(\left(X_{1}-\mathbb{E}\left(X_{1}\right)\right)^{2}\right) \text { as } n \rightarrow \infty, \text { if } \mathbb{E}\left(X_{1}^{4}\right)<\infty$$
Estimate [[Verteilungsfunktion|CDF]]:
$$F_{n}\left(t ; X_{1}, \ldots, X_{n}\right): \mu=F(t), \quad \sigma_{n}^{2}=F(t)(1-F(t)) / n$$

## Their Distribution

For very large $n$ they are approximately **normally distributed** with the above [[Erwartungswert|Expectation]] and [[Varianz|Variance]].

$n F_n\left(t ; X_1, \ldots, X_n\right)$ has [[Binomialverteilung|Binomial Distribution]] with $n=n$ and $p=F(t)$. So at a given point $t$ we can approximate a [[Binomialverteilung|Binomial Distribution]] with the [[Empirical cumulative distribution functions|ECDF]] times $n$.

If all datapoints come from a [[Normalverteilung|Normal Distribution]], then the [[Sample Variance]] has [[Chi-Squared Distribution]]:
$$\Gamma\left(\frac{n-1}{2}, \frac{1}{2}\right)=: \chi_{n-1}^2$$
with $n-1$ [[Degrees of Freedom]].
