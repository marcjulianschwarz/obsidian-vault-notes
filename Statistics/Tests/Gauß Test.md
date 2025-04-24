---
uni-module: "ISSP"
---

# Gauß Test

Good approximation if [[Entity|sample]] size is large. Can be applied for lots of problems.
Indirect Reasoning → Adopt point of other "person"

- [[One-Sided Gauß Test]]
	- [[Left-Sided Gauß Test]]
	- [[Right-Sided Gauß Test]]
- [[Two-Sided Gauß Test]]

## Derivation of Test Statistic and Power Function

We know that the [[Arithmetic Mean]] from the [[Standard Estimators]] has [[Normalverteilung|Normal Distribution]] with [[Varianz|Variance]] $\sigma^2/n$.

So we can now calculate the Standardized Mean (comes from subtracting the mean and dividing by the square root of the variance) looks like this:
$$T_{n}:=\frac{\bar{X}_{(n)}-\mu_{0}}{\sigma / \sqrt{n}}$$
This now has [[Standardnormalverteilung|Standard Normal Distribution]] with its corresponding [[Verteilungsfunktion|CDF]] and p-quantiles.

We now want to create a new [[Zufallsvariable|Random Variable]] which is the standardized $T_n$ plus the standardized distance between the two expectations from the hypothesis.

$$Z=T_n+\frac{\mu-\mu_0}{\sigma}\sqrt{n}=T_n+\lambda$$
$$P_{\mu}(Z\leq z)=P_{\mu}(T_n+\lambda\leq z)$$
We know the [[Wahrscheinlichkeitsmaß|distribution]] of $T_n$ which is the standard normal distribution. We thus want to reformulate the equation to:
$$P_{\mu}(T_n\leq z-\lambda)$$
which we now know the [[Wahrscheinlichkeitsmaß|distribution]] of.
We can write
$$P_{\mu}(T_n\leq z-\lambda)=\phi(z-\lambda):=\phi_{\lambda}(z)$$
So basically a normal distribution which depends on the difference between the measured and real expectations.

$\phi_{\lambda}$ is strictly monotonically decreasing in $\mu$ which comes from the definition of $\lambda$. We can use this new definition of the [[Test Statistic]] $Z$ to define and draw the [[Power Function]].

## Other References

- https://de.wikipedia.org/wiki/Gauß-Test
- https://en.wikipedia.org/wiki/Student%27s_t-test → basically Gauß Test but for other non normal distributions or normal distributions with skewed variance
- https://en.wikipedia.org/wiki/Z-test
