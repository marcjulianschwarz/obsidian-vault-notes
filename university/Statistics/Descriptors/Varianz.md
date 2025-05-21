---
uni-module: "StochMod"

alias: "Variance"
---

# Varianz

Die Varianz gibt an wie die [[Wahrscheinlichkeitsmaß|Verteilung]] einer [[Zufallsvariable]] um den [[Erwartungswert]] verteilt ist.

Falls eine endliche Varianz existiert gelten folgende Definitionen. Damit eine Varianz endlich ist muss auch der [[Erwartungswert]] endlich und existent sein.

The variance of a data sequence is often called [[Sample Variance]].

## Definitionen

$$\operatorname{Var} X=E\left[(X-E X)^{2}\right] \in[0,+\infty]$$
$$\operatorname{Var} X=E\left[X^{2}\right]-(E X)^{2}$$
Mithilfe der Varianz lässt sich die [[Standardabweichung]] definieren.

Die Varianz ist die [[Kovarianz]] von zwei gleichen [[Zufallsvariable|Zufallsvariablen]].

## Properties of Variance

$$
\begin{aligned}
&\operatorname{Var}(X+a)=\operatorname{Var} X \\
&\operatorname{Var}(bX)=b^{2} \operatorname{Var}(X)
\end{aligned}
$$

$$\mathbb{V}(Y+Z)=\mathbb{E}\left((Y-\mathbb{E}(Y)+Z-\mathbb{E}(Z))^2\right)=\mathbb{V}(Y)+\mathbb{V}(Z)+2 \operatorname{Cov}(Y, Z)$$
So if the two random variables are uncorrelated we get

$$
\mathbb{V}(c Y+d Z)=c^2 \mathbb{V}(Y)+d^2 \mathbb{V}(Z)
$$
