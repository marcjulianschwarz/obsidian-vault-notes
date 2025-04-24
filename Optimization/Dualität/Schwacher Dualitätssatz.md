---
uni-module: "LNS"
---

# Schwacher Dualitätssatz

Ist $x$ zulässig für das primale Problem und $(\lambda, \mu)$ zulässig für das duale Problem, dann gilt:
$$p(\bar{x})=f(\bar{x}) \geq d(\bar{\lambda}, \bar{\mu})$$
**Also das duale Problem ist eine untere Schranke für den optimalen ZFW des primalen Problems.**

Für ein typisches [[Lineares Optimierungsproblem|LP]]:
$$b^{\top} y \leq c^{\top} x \quad \text { für alle } x \in \mathcal{F} \text {. }$$

_Beweis:_
Da alle Gleichungsnebenbedingungen gleich 0 sind und alle Ungleichungsnebenbedingungen kleiner gleich 0 sind und alle $\mu \ge 0$ sind, gilt:
$$d(\bar{\lambda}, \bar{\mu})=\inf _{x \in \mathbb{R}^{n}} \mathcal{L}(x, \bar{\lambda}, \bar{\mu}) \leq \mathcal{L}(\bar{x}, \bar{\lambda}, \bar{\mu})=f(\bar{x})+\underbrace{\bar{\lambda}^{\top} h(\bar{x})}_{=0}+\underbrace{\bar{\mu}^{\top} g(\bar{x})}_{\leq 0} \leq f(\bar{x})=p(\bar{x}) .$$
