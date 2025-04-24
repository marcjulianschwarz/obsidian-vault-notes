---
uni-module: KRY
aliases:
  - Square-And-Multiply-Methode
tags:
  - Algorithmus
---

# Square-And-Multiply-Methode zum Potenzieren

Eine Methode um schnell
$$a^d\bmod n$$
zu berechnen.

Diese Methode lässt sich [[Rekursion|rekursiv]] definieren als:

$$c_0=a\bmod n$$
$$c_{i+1}=c_i^2\bmod n$$
$$d_0=d$$
$$d_{i+1}=\lfloor\frac{d_i}{2}\rfloor$$
$$\delta_i=d_i \bmod 2$$
$$b_0=a^{\delta_0}\bmod n$$
$$b_{i+1}=b_ic_{i+1}^{\delta_{i+1}}\bmod n$$
Ist $d_i \leq 1$, so ist $b_i=a^d\bmod n.$

## [[Laufzeit]]

Die [[Laufzeit]] ist durch die Größe von $d$ beschränkt. In jeder Iteration wird $d_i$ halbiert.
Wir berechnen also schnell, dass wir nur
$$l=\lfloor\log_2d\rfloor<3.33\log_{10}d$$
Schleifenwiederholungen brauchen.
Wir müssen also $l$ mal ein Quadrat bilden und höchstens $l$ Multiplikationen durchführen.

Die Laufzeit lässt sich also mit $O((\log n)^3)$ abschätzen.

## Variante 2

In der zweiten Variante versuchen wir den Exponenten stückweise kleiner zu machen. Dabei müssen wir dann immer nur kleine Potenzen berechnen, da die [[Modulo]] Operation die Zahlen immer kleiner gleich $n$ hält.

Wir verwenden also einmal für gerades $d$
$$b \cdot c^d \equiv b \cdot\left(c^2 \bmod n\right)^{\frac{d}{2}} \bmod n$$
und für ungeraded $d$
$$b \cdot c^d \equiv(b c \bmod n) \cdot c^{d-1} \bmod n.$$
Algorithmisch lässt sich auch dieses Verfahren rekursiv definieren, mit:

$$b_0=1, \quad c_0=a\bmod n,\quad d_o=d.$$
Wenn $d_i=0$, dan ist $b_i=a^d\bmod n$.

Für $d_i>0$ und $d_i$ **gerade**:
$$b_{i+1}=b_i, \quad c_{i+1}=c_i^2 \bmod n, \quad d_{i+1}=\frac{d_i}{2}.$$
Für $d_i >0$ und $d_i$ **ungerade**:
$$b_{i+1}=b_i c_i \bmod n, \quad c_{i+1}=c_i, \quad d_{i+1}=d_i-1.$$

#code paste here

## Variante 3

#code paste here
