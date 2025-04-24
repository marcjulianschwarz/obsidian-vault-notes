---
uni-module: "ISSP"
---

# Lilliefors Test of Normality

Test for class of normal distributions.

We can write the class or set of normal distributions as:
$$\left\{N\left(\mu, \sigma^2\right) \mid \mu \in \mathbb{R}, \sigma^2>0\right\}$$

Our [[Null Hypothesis]] thus is
$$H_0:F\in \left\{N\left(\mu, \sigma^2\right) \mid \mu \in \mathbb{R}, \sigma^2>0\right\}$$
or in words, "is the CDF of our data sequence in the class of normal distributions?"

We define our [[Test Statistic]] $L_n$ as the supremum of the absolute distances between the [[Empirical cumulative distribution functions|ECDF]] and the [[Verteilungsfunktion|CDF]] of a normal distribution with [[Standard Estimators|estimated]] [[Arithmetic Mean]] and Variance.

The distribution of $L_n$ is [[stochastisch unabhängig|independent]] of the [[Varianz|Variance]] and [[Erwartungswert|Expectation]] of the [[Normalverteilung|Normal Distribution]] and may thus be simulated.

To make up for the increasing $n$ we use the square root of it to scale the distribution.

We **accept** $H_0$:

- if the test statistic is $\leq \frac{L_{1-\alpha}}{\sqrt{n}}$
- if $\alpha < p(l)$ with $p(l)=1-L(\sqrt{n}l)$ the [[p-Value]] of the test.

## Usage in R

#todo

```R

```
