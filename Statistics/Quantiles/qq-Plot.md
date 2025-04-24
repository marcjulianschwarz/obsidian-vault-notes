---
uni-module: "ISSP"
---

# qq-Plot

When $F=G$ then their qq-plot is on the diagonal.

The deviation of the diagonal can yield qualitative information about the CDFs.

## Normality Testing

Use this R code to test if given data sequence comes from a [[Normalverteilung|Normal Distribution]]:

```R
mu = 2
sug = 13

x = rnorm(10000, mu, sig)
qqnorm(x)
abline(mu, sig)
```

See [[Shapiro-Wilk Test of Normality]] for a way to transform this rather subjective test into a statistical test.

### Other Distributions

For other qq-plots use the R package `car` with `qqPlot(x, dist="unif")` as an example.

## Compare equality of two distributions

Determine if data sequence from strictly monotonic CDF $F$:

$$\left\{\left(Q_{F}^{-}\left(\frac{k-1 / 2}{m}\right), x_{(k)}\right) \mid k \in\{1, \ldots, m\}\right\}$$
Determine if two data sequences from the same strictly monotonic CDF:

$$\left\{\left(Q_{F_{n}(\cdot ; y)}^{-}\left(\frac{k-1 / 2}{m}\right), x_{(k)}\right) \mid k \in\{1, \ldots, m\}\right\}$$

## CDFs with plateau

We only have convergence for CDFs which are strictly monotonic. We thus need to use a pp-Plot which displays the two [[Wahrscheinlichkeitsmaß|distribution]] functions against each other.
