---
uni-module: "LNS"
---

# Innere-Punkte-Verfahren für restringierte Optimierungsprobleme

## Primal-duale Verfahren für lineare Optimierungsprobleme

Eine Unterklasse der [[Innere-Punkte-Verfahren]] sind die [[Primal-Duale Verfahren|primal dualen Verfahren]].
Ein Beispiel dafür ist das [[Primal-duales pfadfolgendes Innere-Punkte-Verfahren]].

Mit der [[Primal-dual zulässige Menge]], dem [[Zentraler Pfad]] und dessen [[Nachbarschaft]] können wir das [[Langschritt primal-duales pfadfolgendes Innere-Punkte-Verfahren]] definieren.

## Ein Grundgerüst für nichtlineare Optimierungsprobleme

Auf [[Liniensuchverfahren]] basierendes [[Innere-Punkte-Verfahren]].

$$
\begin{array}{lll}
\min & f(x) & \\
\text { u.d.N. } & h_{j}(x)=0, & j=1, \ldots, m \\
& g_{i}(x)+s_{i}=0, & i=1, \ldots, \ell \\
& s_{i} \geq 0, & i=1, \ldots, \ell
\end{array}
$$

