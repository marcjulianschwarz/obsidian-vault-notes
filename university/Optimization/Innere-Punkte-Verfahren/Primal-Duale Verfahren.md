---
uni-module: LNS
tags:
  - Algorithmus
---

# Primal-Duale Verfahren

Unterklasse der [[Innere-Punkte-Verfahren]].

Lineares Programm in [[Standardform]] mit vollem Zeilenrang.

[[Dualität|Duales]] Programm mit [[Schlupfvariablen]]:

$$
\begin{array}{ll}
\max & b^{\top} \lambda \\
\text { u.d.N. } & A^{\top} \lambda+s=c \\
& s \geq 0
\end{array}
$$

mit [[Karush-Kuhn-Tucker Conditions|KKT]]:

$$
\begin{aligned}
&A x=b, \\
&A^{\top} \lambda+s=c, \\
&x_{i} s_{i}=0, \quad i=1, \ldots n \\
&x, s \geq 0
\end{aligned}
$$

Da wir wissen, dass die Zielfunktion konvex ist und die Nebenbedingungen [[affin-linear]] sind, ist ein Punkt, der die KKT Bedingungen erfüllt direkt ein globales Optimum.

Deswegen definieren wir eine Funktion über alle zulässigen Punkte und [[Lagrange-Multiplikatoren]] um genau diese KKT-Punkte zu finden:

$$
F(x, \lambda, s):=\left(\begin{array}{c}
A^{\top} \lambda+s-c \\
A x-b \\
X S e
\end{array}\right)
$$

mit $X=\operatorname{diag}\left(x_{1}, \ldots, x_{n}\right), S=\operatorname{diag}\left(s_{1}, \ldots, s_{n}\right) \text { und } e=(1, \ldots, 1)^{\top}$

Damit folgt für die [[Karush-Kuhn-Tucker Conditions|KKT]]:

$$
\begin{aligned}
&F(x, \lambda, s)=0 \\
&x, s \geq 0
\end{aligned}
$$

## Allgemeines Vorgehen

1. Suchrichtung bestimmen → mit [[Newton Verfahren]]
2. Maß für den wünschenswertesten Punkt entlang der Suchrichtung → [[Dualitätsmaß]]

Neue Suchrichtung erhalten wir mit [[Jacobi Matrix]] basierend auf dem [[Newton Verfahren]]:

$$
J_{F}(x, \lambda, s)\left(\begin{array}{c}
\Delta x \\
\Delta \lambda \\
\Delta s
\end{array}\right)=-F(x, \lambda, s)
$$

Wir verwenden $r_{b}=A x-b, \quad r_{c}=A^{\top} \lambda+s-c$
und schreiben somit:

$$
\left(\begin{array}{ccc}
0 & A^{\top} & I \\
A & 0 & 0 \\
S & 0 & X
\end{array}\right)\left(\begin{array}{c}
\Delta x \\
\Delta \lambda \\
\Delta s
\end{array}\right)=\left(\begin{array}{c}
-r_{c} \\
-r_{b} \\
-X S e
\end{array}\right)
$$

Wobei die erste Matrix die [[Jacobi Matrix]] von $F$ ist.

Üblicherweise würde ein solcher Schritt $x,s\ge0$ verletzen weswegen wir
$$(x, \lambda, s)+\alpha(\Delta x, \Delta \lambda, \Delta s)$$
für einen Liniensuchparameter $\alpha\in[0,1)$ mit sehr kleinem $\alpha$ verwenden.
Da man so aber nur sehr langsam voran kommt wählen wir $x_{i} s_{i}=\sigma \mu$ wobei $\mu$ das [[Dualitätsmaß]] ist und $\sigma\in[0,1]$ der Zentrierungsparameter. Damit gilt

$$
\left(\begin{array}{ccc}
0 & A^{\top} & I \\
A & 0 & 0 \\
S & 0 & X
\end{array}\right)\left(\begin{array}{c}
\Delta x \\
\Delta \lambda \\
\Delta s
\end{array}\right)=\left(\begin{array}{c}
-r_{c} \\
-r_{b} \\
-X S e+\sigma \mu e
\end{array}\right)
$$

## Algorithmus

[[Primal-duales pfadfolgendes Innere-Punkte-Verfahren]]
