---
uni-module: "ISSP"
---

# Kolmogorov Smirnov Test

Should be used if data sequence is [[Stetigkeit|continous]].

What can we test with this test?

- GOF between two samples
- If one of two samples is stochastically bigger or smaller than the other sample
- GOF for one sample to a certain [[Verteilungsfunktion|CDF]]
- Using [[Lilliefors Test of Normality]] we can test if a sample comes from a class of normal distributions

## GOF

The [[Null Hypothesis]] is
$$H_{0}:F=G$$

The [[Test Statistic]] is given by the theorem of [[Glivenko-Cantelli]] with

$$D_n\left(X_1, \ldots, X_n\right):=\sup _{t \in \mathbb{R}}\left|F_n\left(t ; X_1, \ldots, X_n\right)-F(t)\right|$$

Given $H_{0}$ the test statistic should be small.

We can implement a supremum function in R like this:

```R
sup = function(x, F){
  fn = ecdf(x)
  xi = c(knots(fn),Inf)
  eta = c(-Inf, knots(fn))
  max(abs(fn(xi) - F(xi)), abs(fn(eta) - F(xi)))
}
```

where `knots` gives the jump positions of a function.
One can then use the function to get the supremum of the differences between the [[Empirical cumulative distribution functions|ECDF]] $x$ and a [[Verteilungsfunktion|CDF]] like this:

```R
sup(x, function(t) punif(t))
```

We have for the slightly changed Test Statistic (multiplied by $\sqrt{n}$) :
$$\lim _{n \rightarrow \infty} \mathbb{P}\left(\sqrt{n} D_n\left(X_1, \ldots, X_n\right) \leq t\right)=K(t)$$
where $K(t)$ is the [[Kolmogorov Distribution]].

---

We can also test the [[Null Hypothesis]]
$$H_0:F\leq G$$ with the [[Test Statistic]]
$$D_n^{+}:=\sup _{t \in \mathbb{R}}\left(F_n\left(t ; X_1, \ldots, X_n\right)-F(t)\right)$$
for which we can simulate the [[Wahrscheinlichkeitsmaß|Distribution]] with any [[Stetigkeit|continous]] [[Wahrscheinlichkeitsmaß|distribution]] as it is independent on the underlying [[Wahrscheinlichkeitsmaß|distribution]] if it is continous.

Now for large $n$ the distributon will have an explicit approximate form, a variation of the [[Kolmogorov Distribution]]:
$$K^{+}(t)=\left(1-e^{-2 t^2}\right) 1_{(0, \infty)}(t)$$

## How to perform the test

- Formulate [[Null Hypothesis]]
- Fix probability of [[Type 1 Error]]
- Determine $1-\alpha$ [[Perzentil|Quantile]] of the [[Kolmogorov Distribution]]
- Perform experiment and calculate [[Test Statistic]]
- accept $H_{0}$ if
  $$D_n\left(x_1, \ldots, x_n\right) \leq \frac{K_{1-\alpha}}{\sqrt{n}}$$

## Test of Equality of two continous distributions

$$H_0:F=G$$

[[Test Statistic]]

## In R

Test if equal

```R
x = rnorm(100)
y = rnorm(100, 0.2, 1.1)

ks.test(x=x, y=y, alternative="two.sided")
```

Test if equal to some CDF

```R
x = rnorm(100)

ks.test(x=x, "norm", alternative="two.sided")
```

Test if less or greater:

```R
x = rnorm(100)
y = rnorm(100, 0, -1)

ks.test(x=x, y=y, alternative="l")
ks.test(x=x, y=y, alternative="g")
```
