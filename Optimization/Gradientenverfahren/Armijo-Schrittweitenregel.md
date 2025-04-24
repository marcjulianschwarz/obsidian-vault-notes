---
uni-module: "LNS"
---

# Armijo-Schrittweitenregel

Seien $\beta\in(0,1)$ und $\gamma\in(0,1)$ fest gewählte Parameter. Zum Beispiel $\beta = \frac{1}{2}$ und $\gamma = 10^{-2}$.

Bestimme die größte Zahl $\sigma_k\in\set{1,\beta,\beta^2,...}$ für die gilt:

$$f\left(x^{(k)}+\sigma_{k} s^{(k)}\right)-f\left(x^{(k)}\right) \leq \sigma_{k} \gamma \nabla f\left(x^{(k)}\right)^{\top} s^{(k)}$$
Also implementiert als:
Solange die Bedingung nicht gilt: multipliziere sigma mit beta.


