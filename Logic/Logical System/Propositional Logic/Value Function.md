---
uni-module: "AI"
---

# Value Function

Assigns values to well-formed [[Propositional Logic]] formulas. It is recursively defined and uses the [[Interpretation Function]] to give meaning to the connectives and the [[Variable Assignment]] function to assign values to variables.

$$
\begin{aligned}
& \mathcal{I}_{\varphi}(P)=\varphi(P) \\
& \mathcal{I}_{\varphi}(\neg \mathrm{A})=\mathcal{I}(\neg)\left(\mathcal{I}_{\varphi}(\mathrm{A})\right) \\
& \mathcal{I}_{\varphi}(\mathrm{A} \wedge \mathrm{B})=\mathcal{I}(\wedge)\left(\mathcal{I}_{\varphi}(\mathrm{A}), \mathcal{I}_{\varphi}(\mathrm{B})\right)
\end{aligned}
$$
