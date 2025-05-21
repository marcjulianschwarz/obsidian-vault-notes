---
uni-module: "LNS"
---

# Uncapacitated Facility Location Problem

Kunden werden von Depots mit Fixkosten und Transportkosten beliefert.

$$
\begin{array}{lr}
\min
\sum_{i=1}^{m} \sum_{j=1}^{n} c_{i j} x_{i j}+\sum_{j=1}^{n} f_{j} y_{j} & 1 \leq i \leq m \\
\sum_{j=1}^{n} x_{i j}=1 & 1 \leq j \leq n \\
\sum_{i=1}^{m} x_{i j} \leq m y_{j} & 1 \leq i \leq m, 1 \leq j \leq n \\
x_{i j} \geq 0 & 1 \leq j \leq n .
\end{array}
$$

1. Nebenbedingung → Ein Kunde wird nur von genau einem Depot beliefert
2. Nebenbedingung → Ein Depot muss genutzt werden wenn ein Kunde von dort belifert wird → Ähnlich wie bei [[Uncapacitated Lot-Sizing Problem]] und [[Capacitated Lot-Sizing Problem]]
