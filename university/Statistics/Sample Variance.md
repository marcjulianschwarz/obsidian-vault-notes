---
uni-module: "ISSP"
---

# Sample Variance

## Empirical Sample Variance

$$
\begin{equation}
s_{n}^{2}=\frac{1}{n-1} \sum_{i=1}^{n}\left(X_{i}-\bar{X}_{(n)}\right)^{2}
\end{equation}
$$

$$V(t)=\frac{1}{n} \sum_{k=1}^n\left(t_k-M(t)\right)^2$$

**Properties**
If we have $\mathbb{E}\left(X_1^4\right)<\infty$ , then for the [[Sample Variance]] $S^2_{(n)}$ we have:
$$\mathbb{E}\left(S_{(n)}^2\right)=\sigma^2, \quad \mathbb{V}\left(S_{(n)}^2\right)=\frac{1}{n}\left(\mathbb{V}\left(\left(X_1-\mu\right)^2\right)+\frac{2}{n-1} \sigma^4\right)$$
_The [[Erwartungswert|Expectation]] is exactly the value we want to estimate. We can use the [[Varianz|Variance]] to further describe the behaviour of the estimator._
