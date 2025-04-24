---
uni-module: "LNS"

alias: ["MIP", "MIPs", "Mixed Integer Program"]
---

# Gemischt-ganzzahliges Optimierungsproblem

Ein Optimierungsproblem mit $x$ gemischt-ganzzahlig und linearen Nebenbedingungen

$$
\begin{aligned}
\min  c^{\top} x \\
& A x \leq b \\
& x \in \mathbb{Z}^{p} \times \mathbb{R}^{n-p}
\end{aligned}
$$

## Spezialfälle

- $p=0$ → [[Lineares Optimierungsproblem|Linear Program]]
- $p=n$ → [[Integer Program]]
- $p=n$ und $x\in\set{0,1}^n$ → [[Binary Integer Program]]

## Beispiele

- [[Uncapacitated Lot-Sizing Problem]]
- [[Capacitated Lot-Sizing Problem]]
- [[Traveling Salesman Problem]]
- [[Uncapacitated Facility Location Problem]]
- [[Knapsack Problem]]
