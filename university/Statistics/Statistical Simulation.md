---
uni-module: "ISSP"
---

# Statistical Simulation

Generate random Numbers from a given [[Wahrscheinlichkeitsmaß|distribution]] $F$ by applying its [[Quantile Function]] on a [[Zufallsvariable|Random Variable]] $X$ that has [[Gleichverteilung|Uniform Distribution]] on $(0,1)$

$$
Y:=Q_F^{-}(X):=Q_F^{-} \circ X.
$$

$Y$ now has [[Verteilungsfunktion|CDF]] $F$.

This also works the other way around.

**How do we get good random numbers from a [[Gleichverteilung|Uniform Distribution]] on $(0,1)$?**

- random physical process
- deterministic pseudo random numbers
- coin tossing for digits in binary
- erasing leading digits of random numbers with a density
