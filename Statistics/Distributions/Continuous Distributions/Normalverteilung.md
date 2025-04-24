---
uni-module: "StochMod"

alias:
  [
    "Gauß-Verteilung",
    "Gaußsche Normalverteilung",
    "Standardnormalverteilung",
    "Normal Distribution",
    "Gaussian",
    "Gaussian Distribution",
  ]
---

# Normalverteilung

Für $\mu\in\mathbb{R}$ und $\sigma^2>0$:
$$f(x)=\frac{1}{\sqrt{2 \pi \sigma^{2}}} e^{-\frac{1}{2} \frac{(x-\mu)^{2}}{\sigma^{2}}}, x \in \mathbb{R}$$

Wir schreiben auch:
$$N(\mu,\sigma^2)$$

Der Spezialfall $\mu=0,\sigma^2=1$ also $N(0,1)$ heißt Standardnormalverteilung.

[[Verteilungsfunktion|CDF]]:
$$F(x)=\frac{1}{\sqrt{2 \pi}} \int_{-\infty}^{x} e^{-\frac{1}{2} y^{2}} d y, x \in \mathbb{R}$$

![[Bildschirmfoto 2022-05-02 um 10.51.53.png]]
