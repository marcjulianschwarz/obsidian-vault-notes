---
uni-module: "ISSP"
---

# One-Sided t-Test

[[Test Statistic]] given by
$$T_n:=\frac{\bar{X}_{(n)}-\mu_0}{\sqrt{S_{(n)}^2 / n}}$$
where we estimate the [[Varianz|Variance]] by the [[Sample Variance]].

The [[Test Statistic]] has [[t-Distribution]] for $\mu=\mu_0$ with $n-1$ [[Degrees of Freedom]].
For $\mu\neq\mu_0$ we have to use the [[Non-Centrality Parameter]]
$$\lambda=\sqrt{n}\left(\mu-\mu_0\right) / \sigma.$$

## Confidence Interval

[[Confidence Interval]] can be calculated like this:

![[Bildschirm­foto 2023-02-10 um 10.55.34.png]]
