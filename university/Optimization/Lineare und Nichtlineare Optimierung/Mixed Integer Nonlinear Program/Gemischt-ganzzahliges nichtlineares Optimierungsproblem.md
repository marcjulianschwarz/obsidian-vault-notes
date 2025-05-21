---
uni-module: "LNS"

alias: ["MINLP", "MINLPs", "Mixed-Integer Nonlinear Program"]
---

# Gemischt-ganzzahliges nichtlineares Optimierungsproblem

Im Vergleich zu [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIPs]] kann bei [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLPs]] die Zielfunktion und die Nebenbedingungen auch nicht linear sein.

Beispiel: [[Pooling-Problem]]

## Allgemeine Form

$$
\begin{array}{cl}
\min _{x, z} & f(x, z) \\
\text { s.t. } & c_{i}(x, z) \leq 0, \quad i \in \mathcal{I} \\
& (x, z) \in P \\
& l \leq z \leq u \\
& x \in \mathbb{R}^{n}, z \in \mathbb{Z}^{m}
\end{array}
$$

- $f$ ist möglicherweise nichtlinear
- $\mathcal{I}$ ist eine endliche Indexmenge
- $c_i$ möglicherweise nichtlinear
- $P$ ist [[Polytop]]
- $l,u$ mit $l\le u$ → also alle ganzzahligen Variablen sind nach oben und unten beschränkt

## Konvexität

Man unterscheidet zwischen [[Konvexe Funktion|konvexen]] und nicht konvexen [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLPs]] wobei hierbei zu beachten ist, dass damit nur gemeint ist, dass das Problem ohne Ganzzahligkeitsbedinung konvex ist. Das ist der Fall, wenn die Funktionen $f$ und $c_i$ konvex sind.

Die Zielfunktion und Nebenbedingungen können durch [[Konvexe Relaxierung]] konvexifiziert werden.

## Schnittebenenverfahren

Kann das [[Separierungsproblem|Schnittebenenverfahren]] auf [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLPs]] angewendet werden?

Ja, aber nur wenn die Zielfunktion linear ist.
Eine nichtlineare Zielfunktion lässt sich aber wie folgt umformulieren:

$$
\begin{array}{ll}
\min _{x, z, \eta} & \eta \\
\text { s.t. } & \eta \geq f(x, z), \\
& c_{i}(x, z) \leq 0, \\
& (x, z) \in P \\
& l \leq z \leq u \\
& x \in \mathbb{R}^{n}, z \in \mathbb{Z}^{m}, \eta \in \mathbb{R} .
\end{array}
$$
