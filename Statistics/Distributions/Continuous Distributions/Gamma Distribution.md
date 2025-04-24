---
uni-module: "ISSP"
---

# Gamma Distribution

Position of $r^{th}$ random point.

$$f(x)=\frac{\lambda^r}{\Gamma(r)} x^{r-1} e^{-\lambda x} 1_{[0, \infty)}(x)$$
[[Gamma Function]]

r-fold sum of [[stochastisch unabhängig|independent]] [[Exponentialverteilung|Exponential Distributions]] with parameter $\lambda$.

We have

$$
\left\|F_{N B(r, p)}-F_{\Gamma(r, p)}\right\|_{\infty} \leq r \frac{p}{1-p}
$$
