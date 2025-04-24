---
uni-module: "LNS"
---

# Konstruktionsheuristik

[[Heuristik]], die möglichst schnell eine (gute) zulässige Lösung findet.

[[Heuristik|Heuristiken]], die anhand eines [[Binary Integer Program|BIP]]:

$$\min \left\{c^{\top} x: x \in X\right\}, \quad X=\left\{x \in\{0,1\}^{n}: A x \geq b\right\}$$
mit [[LP-Relaxierung]]
$$\min \left\{c^{\top} x: x \in P\right\}, \quad P=\left\{x \in[0,1]^{n}: A x \geq b\right\}$$
arbeitet.

- [[Tauchheuristik]]
  - [[Dive-and-Fix]]
- [[Feasibility Pump]]
