---
uni-module: MFDS
---

# Partialbruchzerlegung

$$
\begin{equation}
r(x):=\frac{p(x)}{q(x)}=\frac{p(x)}{\tilde{q}(x) \cdot\left(x-x_{1}\right)^{k}}
\end{equation}
$$

$$
\begin{equation}
r(x)=\frac{p(x)}{\tilde{q}(x)\left(x-x_{1}\right)^{k}}=\frac{\tilde{p}(x)}{\tilde{q}(x)}+\sum_{j=1}^{k} \frac{A_{j}}{\left(x-x_{1}\right)^{j}}
\end{equation}
$$

$$
\begin{equation}
\frac{p(x)}{q(x)}=\sum_{i=1}^{k} \sum_{j=1}^{s_{i}} \frac{A_{j}^{(i)}}{\left(x-x_{i}\right)^{j}}+\sum_{i=1}^{l} \sum_{j=1}^{t_{i}} \frac{B_{j}^{(i)} x+C_{j}^{(i)}}{\left(x^{2}-2 a x+b\right)^{j}}
\end{equation}
$$

## Algorithmus

1. In eine eindeutige Darstellung bringen (echt gebrochen rational). Zählergrad größer als Nennergrad.
2. Nullstellen des Nennerpolynoms bestimmen.
3. Bestimmung der Partialbruchzerlegung
4. [[Lineares Gleichungssystem]] durch Koeffizientenvergleich aufstellen
5. Das Gleichungssystem lösen
6. Integral der Summe einfacher Terme lösen
