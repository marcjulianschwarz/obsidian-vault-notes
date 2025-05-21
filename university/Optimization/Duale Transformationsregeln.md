---
uni-module: "LKO"
---

# Duale Transformationsregeln

Mit diesen Regeln lässt sich ein primales Problem in ein [[Dualität|duales]] Problem umwandeln. Das kann dann zum Beispiel mit dem [[Der duale Simplex-Algorithmus|dualen Simplex]] gelöst werden.

$$
\begin{array}{rll}
\hline \text { Primal } & & \text { Dual } \\
\hline \text { Ungleichung } & \leftrightarrow & \text { nicht-negative Variable } \\
\text { Gleichung } & \leftrightarrow & \text { freie Variable } \\
\text { nicht-negative Variable } & \leftrightarrow & \text { Ungleichung } \\
\text { freie Variable } & \leftrightarrow & \text { Gleichung } \\
\hline
\end{array}
$$

## Primales Problem

$$
\begin{array}{ll}
\min _{x, y} & c^{\top} x+d^{\top} y \\
\text { s.t. } & A x+B y \geq a \\
& C x+D y=b \\
& x \geq 0
\end{array}
$$

## Duales Problem

$$
\begin{array}{ll}
\max _{u, v} & a^{\top} u+b^{\top} v \\
\text { s.t. } & A^{\top} u+C^{\top} v \leq c \\
& B^{\top} u+D^{\top} v=d \\
& u \geq 0
\end{array}
$$
