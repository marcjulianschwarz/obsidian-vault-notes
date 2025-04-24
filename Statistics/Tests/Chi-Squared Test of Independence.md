---
uni-module: "ISSP"
---

# Chi-Squared Test of Independence

Tests if two [[Zufallsvariable|Random Variables]] $(X,Y)$ are independent.

- Partition both random variables into sets (already done for discrete random variables)
- Calculate [[Joint Class Probability|Joint Class Probabilities]]
- Calculate [[Margin Class Probability]]

If $X,Y$ are [[stochastisch unabhängig|independent]], then the [[Joint Class Probability]] is the same as the product of the [[Margin Class Probability|Margin Class Probabilities]]. Thus the [[Null Hypothesis]] is:
$$H_0: p_{i j}=p_{i \bullet} \cdot p_{\bullet j}.$$

Given $H_{0}$ the [[Test Statistic]]
$$T_n=\sum_{i=1}^r \sum_{j=1}^s \frac{\left(N_{i j}-n \frac{N_{i \bullet}}{n} \frac{N_{\bullet j}}{n}\right)^2}{n \frac{N_{i \bullet}}{n} \frac{N_{\bullet j}}{n}}$$
should be small.

We can simulate the test statistic by drawing with replacement from box with $r\times s$ types of balls with [[Relative Häufigkeit|Relative Frequencies]] $p_{i \bullet} \cdot p_{\bullet j}$ . For large $n$ the [[Wahrscheinlichkeitsmaß|distribution]] is actually [[stochastisch unabhängig|independent]] on the probabilities.

The [[Wahrscheinlichkeitsmaß|distribution]] converges to the [[Chi-Squared Distribution]] with $(r-1)\cdot(s-1)$ [[Degrees of Freedom]].

Hence the [[Acceptance Domain]] is asymptoically given by
$$I=\left[0, \chi_{(r-1)(s-1) ; 1-\alpha}^2\right]$$
Without knowing the probabilities the [[Class Condition]] can be checked approximately with
$$n_{ij}\geq 5$$

Another test of independence is the so-called [[Exact Test of Fisher]]

## Application

One can best perform this test using a Contingency Table.
