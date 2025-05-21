---
uni-module: "LNS"
---

# Pooling-Problem

Ähnlich wie Min-Cost-Flow-Problem ([[Graphen Theorie]]).

Zielfunktion ist die Minimierung der Kosten.
Also die _Beschaffungskosten_ (Summe der Kosten für die Rohstoffe entlang des Flusses von Rohstoff zu Pool) minus die _Verkaufserträge_ (Summe der Verkaufspreise der Produkte aus den Pools und Summe der Verkaufspreise der Rohstoffe minus deren Kosten).

$$
\begin{array}{cc}
\min _{p, x, y, z} \underbrace{\sum_{i=1}^{I} c_{i} \sum_{\ell=1}^{L} x_{i \ell}}_{\text {Beschaffungskosten }} \underbrace{-\sum_{j=1}^{J} d_{j} \sum_{\ell=1}^{L} y_{\ell j}-\sum_{i=1}^{I} \sum_{j=1}^{J}\left(d_{j}-c_{i}\right) z_{i j}}_{\text {Verkaufserträge }} \\
\text { s.t. } \sum_{\ell=1}^{L} x_{i \ell}+\sum_{j=1}^{J} z_{i j} \leq A_{i} & i=1, \ldots, I \\
\sum_{i=1}^{I} x_{i \ell}-\sum_{j=1}^{J} y_{\ell j}=0 & \ell=1, \ldots, L \\
\sum_{i=1}^{I} x_{i \ell} \leq S_{\ell} & \ell=1, \ldots, L
\end{array}
$$

$$
\begin{aligned}
&\sum_{\ell=1}^{L} y_{\ell j}+\sum_{i=1}^{I} z_{i j} \leq D_{j} \\
&\sum_{\ell=1}^{L}\left(p_{\ell k}-P_{j k}^{U}\right) y_{\ell j}+\sum_{i=1}^{I}\left(C_{i k}-P_{j k}^{U}\right) z_{i j} \leq 0 \quad j=1, \ldots, J ; \quad k=1, \ldots, K \\
&\sum_{i=1}^{I} C_{i k} x_{i \ell}-p_{\ell k} \sum_{j=1}^{J} y_{\ell j}=0 \\
&x_{i \ell} \geq 0, \quad y_{\ell j} \geq 0, \quad z_{i j} \geq 0, \quad p_{\ell k} \geq 0
\end{aligned}
$$

Nebenbedingung 1:
Der gesamte [[Fluss]] an Rohstoffen muss kleiner gleich der verfügbaren Menge an Rohstoffen sein.

Nebenbedingung 2:
[[Flusserhaltungsbedingung]]

Nebenbedingung 3:
[[Kapazitätsbedingung]]

Nebenbedingung 4:
Fluss an Produkten und Rohstoffen muss kleiner gleich dem [[Bedarfsfunktion|Bedarf]] sein.

Nebenbedingung 5:
Eigenschaften des Gemisches und Eigenschaften der Rohstoffe müssen kleiner gleich der Oberen Schranke der Eigenschaft sein.

Nebenbedingung 6:
Eigenschaftserhaltung

Nebenbedingung 7:
Fluss darf nicht negativ sein und die Eigenschaften des Gemisches müssen positiv sein.

## Allgemeine Darstellung des Problems

![[Bildschirmfoto 2022-07-15 um 09.56.44.png]]
