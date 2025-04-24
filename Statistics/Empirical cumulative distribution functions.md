---
uni-module: "ISSP"

alias: "ECDF"
---

# Empirical cumulative distribution functions

Describes the [[Relative Häufigkeit#Relative Frequency for Interval|relative frequency for every interval]] for a given [[Ordered Data Sequence]].

$$
F_{n}(t):=h_{n}((-\infty, t])=\frac{1}{n} \sum_{i=1}^{n} 1_{(-\infty, t]}\left(x_{i}\right)
$$

- limit to minus infinity goes to 0 and limit to infinity goes to 1.
- it is weackly monotonically increasing
- it is [[right continuous]]
- it is piecewise constant

All of these properties carry over to the [[Verteilungsfunktion|Cumulative Distribution Function]].

[[Relative Häufigkeit|Relative Frequencies]] for intervals can be calculated:
$$h_n((a,b])=F_n(b)-F_n(a)$$

For n to infinity the ECDF converges to the [[Verteilungsfunktion|Cumulative Distribution Function]] (CDF)

**Distribution of Estimator**
For a [[Verteilungsfunktion|CDF]] $F$ of $X_1$ we have [[Erwartungswert|Expectation]] and [[Varianz|Variance]] of an ECDF
$$\mathbb{E}\left(F\left(t ; X_1, \ldots, X_n\right)\right)=F(t), \quad \mathbb{V}\left(F\left(t ; X_1, \ldots, X_n\right)\right)=\frac{F(t) \cdot(1-F(t))}{n}$$

## Proofs

- [[Proof Monotonic Increase]]
- [[Proof of Right Continuity]]
