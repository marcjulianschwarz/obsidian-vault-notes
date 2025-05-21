---
uni-module: "KRY"
---

# Näherungsbruch

Ist $[a_0,a_1,\dots]$ die [[Kettenbruchentwicklung]] einer reellen Zahl $\alpha$, so heißt
$$[a_0,\dots,a_n]$$
der n-te Näherungsbruch.

Sei die [[Kettenbruchentwicklung]] gegeben, dann kann man den Näherungsbruch mit folgenden [[Rekursion|rekursiven]] Regeln berechnen:

$$
\begin{array}{llll}
p_{-2}=0, & p_{-1}=1, & p_n=a_n p_{n-1}+p_{n-2} & \text { für } n \geq 0, \\
q_{-2}=1, & q_{-1}=0, & q_n=a_n q_{n-1}+q_{n-2} & \text { für } n \geq 0
\end{array}
$$

Es gilt dann
$$\left[a_0, a_1, \ldots, a_n\right]=\frac{p_n}{q_n}.$$
