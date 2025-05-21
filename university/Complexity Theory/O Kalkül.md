---
uni-module: LKO

alias: ["Landau Symbole"]
---

# O Kalkül

Diese Notation kann verwendet werden um [[Laufzeitanalyse]] eines Programms oder [[Algorithmus]] zu beschreiben.

$$
\begin{equation}
\begin{aligned}
&f \in O(g) \\
&c f \in O(g) \\
&f+c \in O(g) \\
&f+h \in O(\operatorname{max}(f, h)) \\
&t \cdot h \in O(\text { fh })
\end{aligned}
\end{equation}
$$

$f$ ist in $O(g)$ wenn ein $M$ existiert sodass ab einem $n_0$ gilt
$$|f(n)|\leq g(n).$$

- Eine Folge $a_n$ ist genau dann beschränkt, wenn $a_n\in O(1)$.
- Eine Folge $b_n\in O(\frac{1}{n})$ ist eine Nullfolge.

Es seien
$$f_1(n)=g_1(n)+O\left(h_1(n)\right),$$
$$f_2(n)=g_2(n)+O\left(h_2(n)\right).$$
Dann gilt
$$f_1(n) f_2(n)=g_1(n) g_2(n)+O\left(h_1(n) h_2(n)\right).$$

Polynomial → $O((ln(n))^\lambda)$
Exponentiell → $O(n^\lambda)$

- P → polynomial time
- NP → z.B.: $2^n$
- PSPACE
- EXPTIME → $2^{f(n)}$

## Genauer

$$
\begin{aligned}
&O(g):=\left\{f \in M: \exists C>0, \exists n_{0}>0:|f(n)| \leq C|g(n)| \text { für alle } n \geq n_{0}\right\}, \\
&\Omega(g):=\left\{f \in M: \exists c>0, \exists n_{0}>0:|f(n)| \geq c|g(n)| \text { für alle } n \geq n_{0}\right\}, \\
&\Theta(g):=O(g) \cap \Omega(g) .
\end{aligned}
$$
