---
uni-module: "StochMod"
---

# Satz von Berny-Esseen

Folge an [[stochastisch unabhängig]]en [[Zufallsvariable]]n mit identischer [[Wahrscheinlichkeitsmaß|Verteilung]] und zusätzlich gilt: $\delta:=E|X_1-\mu|^3<\infty$ . Dann existiert ein $c>0$:
$$\sup _{x \in\mathbb{R}}\left|P\left(\frac{1}{\sigma \sqrt{n}} \sum_{i=1}^{n}\left(X_{k}-\mu\right) \leq x\right)-\int_{-\infty}^{x} \frac{1}{\sqrt{2 \pi}} e^{-\frac{1}{2} \cdot y^{2}} d y\right|\leq c\frac{\delta}{\sigma^3\sqrt{n}}\quad\forall n\geq1$$
Der genaue Wert von $c$ ist noch unbekannt aber man weiß heute, dass er zwischen $0,4$ und $0,48$ liegt.
