---
uni-module: "LNS"
---

# Basic Mixed Integer Set

Spezielles [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]].
$$X^{M I}=\left\{(s, y) \in \mathbb{R}_{+}^{1} \times \mathbb{Z}^{1}: s+y \geq b\right\}$$

[[Zulässige Ungleichung]]: [[Simple Mixed Integer Rounding Ungleichung]]

[[Polyeder]]

$$
\begin{array}{r}
s+y \geq b \\
s \geq f(\lceil b\rceil-y) \\
s \geq 0
\end{array}
$$

beschreibt $\operatorname{conv}(X^{M I})$.

![[Bildschirmfoto 2022-07-08 um 17.14.01.png]]
