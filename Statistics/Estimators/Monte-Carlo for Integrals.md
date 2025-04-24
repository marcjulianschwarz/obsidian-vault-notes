---
uni-module: "ISSP"
---

# Monte-Carlo for Integrals

Let $X$ be a [[Zufallsvariable|Random Variable]] with [[Gleichverteilung|Uniform Distribution]] on $(0,1)$ and $f$ a continous function on $[0,1]$ , then we can calculate the intergral from $0$ to $1$ of that function using the [[Arithmetic Mean]] as a [[Standard Estimators|Standard Estimator]]:
$$\mathbb{E}(f(X))=\int_0^1 f(x) d x$$

This approach is quite effective for high-dimensional integrals.

```R
x = runif(100000)
mean(sin(x)) - integrate(sin, 0, 1)[1]$value
# 0.00026...
```
