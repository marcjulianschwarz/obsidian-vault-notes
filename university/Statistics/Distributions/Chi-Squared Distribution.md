---
uni-module: "ISSP"
---

# Chi-Squared Distribution

For a sequence of independent [[Zufallsvariable|Random Variables]] that are [[Normalverteilung|normally distributed]].
Then the [[Zufallsvariable|Random Variable]]
$$\sum_{j=1}^{r}{\left(\frac{X_j}{\sigma_j}\right)}$$
has distribution
$$\chi^2_{r,\lambda}$$
with $r$ [[Degrees of Freedom]] and [[Non-Centrality Parameter]]
$$\lambda=\sum_{j=1}^{r}{\left(\frac{\mu_j}{\sigma_j}\right)^2}.$$

When all [[Erwartungswert|Expectations]] in the sequence are the same and $0$, then the distribution has [[Wahrscheinlichkeitsdichte|PDF]]
$$f(x)=\frac{x^{r / 2-1}}{\Gamma(r / 2) 2^{r / 2}} e^{-x / 2} 1_{(0, \infty)}(x)$$
which is also the density of the [[Gamma Distribution]] $\Gamma(r / 2,1 / 2)$.
