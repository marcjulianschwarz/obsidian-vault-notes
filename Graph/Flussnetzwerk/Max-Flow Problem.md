---
uni-module: ["EMD", "LKO"]
---

# Max-Flow Problem

Finde einen [[Maximaler Fluss | Maximalen Fluss]] in einem [[Flussnetzwerk]].

Um dieses Problem zu lösen nutzen wir das Hilfskonstrukt [[Residualnetzwerk]].
Auf einem Residualnetzwerk kann auch einen [[Fluss]] definiert werden.

## Algorithmen

_Primaler Algorithmus_:
[[Ford-Fulkerson Algorithmus]]
_Dualer Algorithmus_:
[[Push-Relabel Algorithmus]]

Die [[Dualität]] des Problems liefert hier also eine obere und untere Schranke für die optimale Lösung.

## Als Lineares Optimierungsproblem

$$
\begin{aligned}
\max _{x \in \mathbb{R}^{|A|}} & \sum_{a \in \delta^{\text {out }}(s)} x_{a}-\sum_{a \in \delta^{\text {in }}(s)} x_{a} \\
\text { s.t. } & 0 \leq x_{a} \leq c_{a} \text { für alle } a \in A, \\
& \sum_{a \in \delta^{\text {in }}(v)} x_{a}=\sum_{a \in \delta^{ \text { out }}(v)} x_{a} \text { für alle } v \in V \backslash\{s, t\} .
\end{aligned}
$$

Überlegen Sie sich, wann dieses [[Lineares Optimierungsproblem|LP]] unbeschränkt ist und welcher Situation im Digraphen D dieses Phänomen entspricht.
