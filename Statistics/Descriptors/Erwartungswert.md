---
uni-module: "StochMod"

alias: "Expectation"
---

# Erwartungswert

Der Erwartungswert gibt den Wert an, der von einer [[Zufallsvariable]] am meisten erwartet wird.

## Diskreter Fall

$$EX:=\sum_{x \in X(\Omega)} x P(X=x)$$
Außerdem gilt:
$$E X=\sum_{\omega \in \Omega} X(\omega) P(\{\omega\})$$

## Reeler Fall

_Definition_ über die [[Verteilungsfunktion]]:
$$EX:=\int_{0}^{\infty}\left(1-F_{X}(x)\right) d x \in[0,+\infty]$$
→ Diese Definition muss für negative Werte der [[Zufallsvariable]] anders verwendet werden. Siehe Skript.

_Definition_ über die [[Wahrscheinlichkeitsdichte]]:
$$EX:=\int_{-\infty}^{\infty} y f_{X}(y) d y$$
→ Diese Definition funktioniert auch automatisch für [[Zufallsvariable|Zufallsvariablen]], die negativ werden können.

## Eigenschaften

Für Beweise zu diesen Eigenschaften siehe S.43ff im Skript. Dabei wird auch das Prinzip der _Approximation durch Summen_ verwendet, welches eventuell hilfreich sein kann als Beweiswerkzeug.

**Monotonicity**
If
$$X(\omega)\leq Y(\omega)$$
, then we have
$$EX\leq EY.$$

**Linearity**
$$E(\alpha X+Y)=\alpha EX + EY$$
**[[stochastisch unabhängig|Independence]]**
$$E(XY)=(EX)(EY)$$
**Function Application**
Wenn $g:(\Omega', \mathcal{A})\rightarrow (\mathbb{R}, \mathcal{B}(\mathbb{R}))$ eine messbare Abbildung ist, dann gilt:
$$E(g(x))=\sum_{x \in X(\Omega)} g(x) P(X=x)$$
