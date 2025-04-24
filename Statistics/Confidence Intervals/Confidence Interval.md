---
uni-module: "ISSP"
---

# Confidence Interval

The [[Confidence Interval]] is more or less the inverse of an [[Acceptance Domain]]

$$t \in A(\vartheta) \Longleftrightarrow \vartheta \in C I(t).$$

This means it contains the most probable parameters given some $t$ from the [[Acceptance Domain]].

From a level-alpha test with [[p-Value]] one can easily derive the [[Confidence Interval]] like this:

$$A(\vartheta)=\left\{t: p_{\vartheta}(t) \geq \alpha\right\} \Longleftrightarrow C l(t)=\left\{\vartheta: p_{\vartheta}(t) \geq \alpha\right\}$$

## General Definition

We have some sample $X_1,\dots, X_n$ from a distribution with parameters $\vartheta \in \Theta$ where $\vartheta$ can for example be the [[Erwartungswert|Expectation]] of a [[Normalverteilung|Normal Distribution]].
Then we can use the sample to create the [[Zufallsvariable|Random Variables]] $U$ and $O$ which as an interval $[U,O]$make up the **random interval of coverage** propability
$$\mathbb{P}_{\vartheta}(\vartheta \in[U, O])$$
It is called the $1-\alpha$ confidence interval for $\vartheta$ if
$$\mathbb{P}_{\vartheta}(\vartheta \in[U, O]) \geq 1-\alpha$$
We want to choose confidence intervals as small as possible.

Using a concrete data sequence, one can say that in about $1-\alpha$ percent of the cases the parameter $\vartheta$ will lie in the interval.

## Examples

See:

- [[Two-Sided Gauß Test]]
- [[One-Sided Gauß Test]]
- [[Two-Sided t-Test]]
- [[One-Sided t-Test]]
- [[Wald-CI]]
- [[Agresti-Cull-CI]]
- [[Asymptotic CI for Variance]]

### Estimate Quantiles of CDF by quantiles of ECDF

$$\mathbb{P}\left(x_p \in\left[X_{(k)}, X_{(\ell)}\right]\right) \geq B(n, p)([k, \ell))$$

With
$$k=\left\lceil n p-z_{1-\alpha / 2} \sqrt{n p(1-p)}\right\rfloor, \quad \ell=\left\lfloor n p+z_{1-\alpha / 2} \sqrt{n p(1-p)}\right\rfloor$$

We get an asymptotically exact $1-\alpha$ CI for the quantile $x_p$.

This approximation is good for
$$np(1-p)\geq 10.$$
