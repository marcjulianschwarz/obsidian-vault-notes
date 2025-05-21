---
uni-module: "LKO"
---

# Minimalkosten-Zirkulations-Problem

[[Zirkulation]]

$\min _{x} \sum_{a \in A} w_{a} x_{a}$
s.t. $x\left(\delta^{\text {out }}(v)\right)-x\left(\delta^{\text {in }}(v)\right)=0 \quad$ für alle $v \in V$,
$d_{a} \leq x_{a} \leq c_{a} \quad$ für alle $a \in A$

Um das Problem in die Form eines Zirkulationsproblems zu bringen fügt man eine neue Kante zwischen der Supersenke und der Superquelle ein. Diese Kante darf natürlich keine Kosten haben und die [[Bedarfsfunktion]] wählt man so, dass der Bedarf der Superquelle dem negativen Bedarf der Supersenke entspricht.

Negative Kosten können so in nicht-negative Kosten transformiert werden:
![[Bildschirmfoto 2022-01-04 um 12.48.42.png]]

## Optimalitätsbedingungen

[[Negative-Kreise-Optimalitätsbedingung]]

Für die weiteren Bedingungen muss zuerst der Begriff [[Reduzierte Kosten]] eingeführt werden.
