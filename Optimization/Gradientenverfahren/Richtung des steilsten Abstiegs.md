---
uni-module: "LNS"

alias: "Direction of Steepest Descend"
---

# Richtung des steilsten Abstiegs

Sei $f$ einmal [[Stetigkeit|stetig]] differenzierbar und $x$ beliebig aber nicht [[Stationärer Punkt|stationär]].

$$\min _{\|d\|=1} \nabla f(x)^{\top} d$$
Jeder Vektor $s=\lambda d$ mit $\lambda\geq 0$ heißt Richtung des steilsten Abstiegs von $f$ in $x$.

Der Vektor $d$ kann eindeutig bestimmt werden durch:
$$d=-\frac{\nabla f(x)}{\|\nabla f(x)\|}$$


[[Abstiegsrichtung]]
