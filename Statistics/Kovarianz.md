---
uni-module:
  - StochMod
aliases:
  - Covariance
---
# Kovarianz

Die Kovarianz gibt an wie sehr zwei [[Wahrscheinlichkeitsmaß|Verteilungen]] von [[Zufallsvariable|Zufallsvariablen]] in ihrer [[Varianz]] um den [[Erwartungswert]] verteilt sind. Ein Spezialfall ist die [[Varianz]].

$$\operatorname{Cov}(X,Y):=E[(X-EX)\cdot(Y-EY)]$$
Sind die [[Varianz|Varianzen]] endlich so gelten folgende _Eigenschaften_:

$$\operatorname{Cov}(X,Y)=E(XY)-E(X)\cdot E(Y)$$
$$\operatorname{Cov}(a X+b, c Y+d)=a c \operatorname{Cov}(X, Y)$$
$$\operatorname{Var}(X+X)=\operatorname{Var}(X)+\operatorname{Var}(Y)+2 \operatorname{Cov}(X, Y)$$

Aus der Kovarianz zusammen mit der [[Varianz]] lässt sich die [[Korrelation]] berechnen.

[[Sample Covariance]]

## Covariance Matrix 

$$X X^T=\sum x_t x_t^T$$
