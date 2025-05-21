---
uni-module: "LNS"
---

# Einführung Spatial Branch-and-Bound Verfahren zur Lösung nichtkonvexer MINLPs

Wir beschränken uns dabei auf [[Faktorisierbar|Faktorisierbare Funktionen]], welche sich mit [[Expression Tree|Expression Trees]] ausdrücken lassen.
Ein [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLP]] mit solchen Funktionen kann in ein äquivalentes Problem mit folgender Form umgewandelt werden:

$$
\begin{array}{ll}
\min _{x, y, z} & y_{q} \\
\text { s.t. } & y_{k}=\vartheta_{k}(x, y, z), \quad k \in\{1, \ldots, q\} \\
& l_{x} \leq x \leq u_{x} \\
& l_{y} \leq y \leq u_{y} \\
& l_{z} \leq z \leq u_{z} \\
& (x, y, z) \in P \\
& x \in \mathbb{R}^{n}, y \in \mathbb{R}^{q}, z \in \mathbb{Z}^{m}
\end{array}
$$

mit $P\subseteq \mathbb{R}^{n+q+m}$ ein [[Polytop]] und $l_{x}, u_{x} \in \mathbb{R}^{n}, l_{y}, u_{y} \in \mathbb{R}^{q}, l_{z}, u_{z} \in \mathbb{R}^{m}$ und $\vartheta\in \mathcal{T}$ für alle $k\in\{1,...,q\}$.

Nun reicht es aus die einzelnen Faktoren der Funktion [[Konkaver Überschätzer|konkav zu überschätzen]] und [[Konvexer Unterschätzer|konvex zu unterschätzen]] um alle Nichtkonvexitäten zu ersetzen.
Dabei kann man zusätzlich entscheiden ob man Ganzzahligkeit relaxiert und ob man nur [[LP-Relaxierung]] oder auch [[NLP-Relaxierung]] zulässt. Je nach Wahl erhält man ein konvexes [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLP]], konvexes [[Nichtlineares Optimierungsproblem|NLP]], [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] oder [[Lineares Optimierungsproblem|LP]].

Die Überlegungen führen uns zum [[Spatial Branch-and-Bound Verfahren]].
