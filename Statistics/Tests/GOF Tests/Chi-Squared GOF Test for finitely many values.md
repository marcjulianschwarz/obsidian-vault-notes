---
uni-module: "ISSP"
---

# Chi-Squared GOF Test for finitely many values

[[Null Hypothesis]]
$$H_{0}:F= G$$

[[Test Statistic]]
$$\sum_{j=1}^{s}{\frac{(N_{j}-np_{j})^2}{np_{j}}}$$

- data sequence size $n$
- frequencies $n_s$ of [[Item Expression]] $\xi_s$ (in [[Zufallsvariable|Random Variable]] $N_j$)
- probability of [[Item Expression]] $p_j$
- Some data sequence from unknown [[Verteilungsfunktion|CDF]] $F$.
- A known discrete [[Verteilungsfunktion|CDF]] $G$

Given $H_0$ the [[Test Statistic]] is small. Thats why the [[p-Value]] is given by
$$p(t)=\mathbb{P}(T_{n}\geq t)$$

We can simulate the test statistic by n-fold drawing with replacement from balls with probability $p_{j}$.

Or use the fact that for $n\rightarrow\infty$ the CDFs of the test statistic will converge to the [[Chi-Squared Distribution]] with $s-1$ [[Degrees of Freedom]]. This approximation is only good if the [[Class Condition]] is met.
Otherwise use simulation above.

## Example Code

Estimate parameters with [[Plug-In-Method]].

```R
N = 6
n = 100

# Data with unknown probability
x = rbinom(n, 5, 0.8)

# Estimate probability
pt = mean(x) / N

# Use estimates proability to get "real" probabilities for all N outcomes
p = dbinom(0:N, N, pt)

# Calculuate the empirical relative frequencies (probabilities) for our data
tab = c()
for (i in 0:N){
  tab[i+1] = sum(x == i)
}

# Calculate Test statistic (more or less: difference between real and empirical probabilities)
T = sum((tab - n*p)**2 / (n*p))
T

# Use CDF of chi squared to determine p-Value of test statistic
pval = 1 - pchisq(T, df=N-1)
pval
```
