---
uni-module: "StochMod"
---

# Relative Häufigkeit Theorie

Zunächst lässt sich die [[Relative Häufigkeit]] durch eine Folge [[stochastisch unabhängig|stochastisch unabhängiger]] [[Zufallsvariable|Zufallsvariablen]] darstellen. Sie bilden vom [[Wahrscheinlichkeitsraum]] $(\Omega',\mathcal{A}',P')$ auf $(\Omega, \mathcal{A},P)$ ab, wobei $P_{X_i}'=P$ ist.
Dann können wir schreiben:
$$H_n(A)=\sum_{i=1}^{n}\mathbb{1}_A(X_i)\cdot\frac{1}{n}$$

Damit unsere Intuition stimmt müsste die Aussage gegen $P(A)$ für $n\rightarrow\infty$ [[Konvergenz|konvergieren]].

Diese [[Konvergenz]] lässt sich auch sinnvoll mit Wahrscheinlichkeiten beschreiben. Man sagt einfach, dass für $n\rightarrow\infty$ die Wahrscheinlichkeit, dass der Fehler der relativen Häufigkeit größer gleich $\epsilon$ ist gleich null sein soll.

[[Ungleichung von Chebyshev]]
