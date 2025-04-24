---
uni-module: "StochMod"

alias: "Binomial Distribution"
---

# Binomialverteilung

Die [[Wahrscheinlichkeitsmaß|Verteilung]] der Anzahl der "Treffer" bei der n-fachen Wiederholung eines Experiments auf einem [[Bernoulli-Raum]]:

$$P(\{k\})=\binom{n}{k}p^k(1-p)^{n-k}$$
mit Parametern $n$ und $p$ → $Bin_{n,p}$

> [!TIP] [[Verteilungsfunktion|CDF]]
>
> $$
> F(x)=\sum_{k=0 \atop k \leq x}^{n}\left(\begin{array}{l}
> n \\
> k
> \end{array}\right) p^{k}(1-p)^{n-k}
> $$

For $n=1$ we get a [[Bernoulli-Verteilung|Bernoulli Distribution]].
