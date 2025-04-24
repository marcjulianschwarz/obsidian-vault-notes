---
uni-module: "StochMod"

alias: "Poisson Distribution"
---

# Poisson Verteilung

$$\mathbb{P}(\{k\})=e^{-\lambda} \frac{\lambda^k}{k !}$$

In der Anwendung ist man oft an Wahrscheinlichkeiten bei Experimenten auf einem [[Bernoulli-Raum]] mit sehr kleinem Parameter $p$ und großem Parameter $n$ interessiert.

Anzahl an Ereignissen in einem fixen Raum.

We have
$$\left\|F_{B(n, p)}-F_{P o(n p)}\right\|_{\infty} \leq 2 n p^2$$


## Annahmen:

- $p$ geht für großes $n$ gegen null
  - Allerdings muss $p_n$ so gewählt werden, dass es nicht zu schnell gegen null [[Konvergenz|konvergiert]]. Das heißt es muss ein $\gamma$ geben, sodass $p_n\cdot n$ gegen $\gamma$ [[Konvergenz|konvergiert]].
- $k$ ist fest

---

Dann lässt sich die [[Binomialverteilung]] in die folgende Form umschreiben:

$$\frac{1}{k!}\frac{n(n-1)...(n-k+1)}{n^k}(np_n)^k(1-\frac{np_n}{n})(1-p_n)^{-k}$$

Dieser Term [[Konvergenz|konvergiert]] für großes $n$ gegen:
$$\frac{1}{k!}\gamma^ke^{-\gamma}$$
für ein $k \in \mathbb{N}_0$

Für einen Parameter $\gamma \in (0,\infty)$ (dieser Wert gibt die bei einer Beobachtung erwartete Ereignishäufigkeit an → [[Erwartungswert]]) heißt die [[Wahrscheinlichkeitsmaß|Verteilung]] Poisson-Verteilung und man schreibt:
$$Poi_\gamma$$
