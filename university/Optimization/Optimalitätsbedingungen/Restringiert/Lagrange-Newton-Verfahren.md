---
uni-module: "LNS"

tags: Algorithmus
---

# Lagrange-Newton-Verfahren

Kann zur Lösung restringierter Probleme verwendet werden, die nur Gleichungsnebenbedingungen haben.

Außerdem müssen die ZF und die Gleichungsnebenbedingungen zweimal [[Stetigkeit|stetig]] differenzierbar sein.

Die [[Karush-Kuhn-Tucker Conditions|KKT]] Bedingungen degenieren dann zu:

$$\nabla\mathcal{L}(x,\lambda)=0$$
$$h(x)=0$$

Dieses Gleichungssystem kann mit dem [[Newton Verfahren]] gelöst werden.

Dafür setzen wir:

$$
R(x, \lambda)=\left(\begin{array}{c}
\nabla_{x} L(x, \lambda) \\
h(x)
\end{array}\right), \quad J_{R}(x, \lambda)=\left(\begin{array}{cc}
\nabla_{x x}^{2} L(x, \lambda) & J_{h}(x)^{T} \\
J_{h}(x) & 0
\end{array}\right)
$$

und lösen dann:

$$J_{R}(x, \lambda) d=-R(x, \lambda)$$

Den neuen Punkt dieser Iterationsfolge erhält man mit $(x,\lambda)+d$ .

$$d=\frac{J_R(x,\lambda)}{-R(x,\lambda)} $$

Diese Iterationsfolge [[Konvergenz|konvergiert]] gegen einen [[Karush-Kuhn-Tucker Conditions|KKT]] Punkt.
Wenn also $f$ konvex ist und alle Nebenbedingungen [[affin-linear]], dann ist dieser Punkt das Optimum.
