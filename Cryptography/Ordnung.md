---
uni-module: "KRY"
---

# Ordnung

Die Ordnung von $a$ modulo $n$ ist das minimale $k$, welches den [[Satz von Euler]] erfüllt.
Wir haben also
$$\operatorname{ord}_n(a)=\min \left\{k \in \mathbb{N}: a^k \equiv 1 \bmod n\right\}.$$

## Eigenschaften

$$a^k \equiv 1 \bmod n \Longleftrightarrow \operatorname{ord}_n(a) \mid k$$
$$\left\{k \in \mathbb{N}: a^k \equiv 1 \bmod n\right\}=\mathbb{N} \cdot \operatorname{ord}_n(a)=\left\{\ell \cdot \operatorname{ord}_n(a): \ell \in \mathbb{N}\right\}$$
Also alle Vielfachen der Ordnung von $a$ modulo $n$ erfüllen auch den [[Satz von Euler]].

$$\operatorname{ord}_n(a) \mid \varphi(n)$$
$$a^{k_1} \equiv a^{k_2} \bmod n \Longleftrightarrow k_1 \equiv k_2 \bmod {\operatorname{ord}_n(a)}$$
Wir können so also leicht im Exponenten rechnen.

$$\operatorname{ord}_n\left(a^k\right)=\frac{\operatorname{ord}_n(a)}{\operatorname{ggT}\left(\operatorname{ord}_n(a), k\right)}$$
Ist $d$ mit $d\mid \operatorname{ord}_n(a)$ , so hat
$$a^{\frac{\operatorname{ord} n(a)}{d}}$$
Ordnung $d$.

## Bestimmung der Ordnung

Ein naives Verfahren bei dem $n$ klein ist oder die Ordnung selbst vermutlich klein ist:

```python

```
