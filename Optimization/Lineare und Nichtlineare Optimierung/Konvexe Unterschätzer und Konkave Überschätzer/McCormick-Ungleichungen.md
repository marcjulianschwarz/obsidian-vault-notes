---
uni-module: "LNS"
---

# McCormick-Ungleichungen

Wir betrachten die Funktion
$$f(x_1,x_2):=x_1x_2$$
mit $f:Q:=\left[\underline{x}_{1}, \bar{x}_{1}\right] \times\left[\underline{x}_{2}, \bar{x}_{2}\right] \rightarrow \mathbb{R}$ .

Wobei $\underline{x}$ die unteren Schranken und $\bar{x}$ die oberen Schranken darstellen.

Die McCormick-Ungleichungen sind:

1. $w\geq\underline{x}_2x_1+\underline{x}_1x_2-\underline{x}_1\underline{x}_2$
2. $w\geq \bar{x}_2x_1+\bar{x}_1x_2-\bar{x}_1\bar{x}_2$
3. $w\leq\underline{x}_2x_1+\bar{x}_1x_2-\bar{x}_1\underline{x}_2$
4. $w\leq \bar{x}_2x_1+\underline{x}_1x_2-\underline{x}_1\bar{x}_2$

Wir können damit also [[konvexe Hülle|konvexe Hüllen]] von [[Bilinearform|bilinearen]] Ausdrücken durch Ungleichungen darstellen.

![[Bildschirmfoto 2022-07-29 um 09.37.43.png]]

_Beweis:_
Berechnung durch verschiedene Kombinationen von
$$0\leq(x_1-\underline{x}_1)(x_2-\underline{x}_2)$$
