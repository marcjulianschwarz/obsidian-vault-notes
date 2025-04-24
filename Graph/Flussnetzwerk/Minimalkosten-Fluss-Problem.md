---
uni-module: "LKO"
---

# Minimalkosten-Fluss-Problem

_Minimiere über den Fluss, sodass die Kosten_ $w_a$ _minimal werden_
$\min _{x} \sum_{a \in A} w_{a} x_{a}$

_Nebenbedingungen_
s.t.
_Die [[Bedarfsfunktion]] muss erfüllt werden._
$x\left(\delta^{\text {out }}(v)\right)-x\left(\delta^{\text {in }}(v)\right)=b(v)$ für alle $v \in V$,
_Die [[Kapazitätsbedingung]] muss natürlich auch gelten_
$0 \leq x_{a} \leq c_{a} \quad$ für alle $a \in A$

## Reformulierungen

### auf (s-t)-Problem

Zum eingrenzen der [[Bedarfsfunktion]] können Superquellen und Supersenken verwendet werden. Diese verbinden alle Quellen und Senken jeweils zu einem Knoten.
Die Bedarfsfunktionen werden jeweils so gewählt, dass der Bedarf an den Quellen und Senken Null ist. Die Superquelle speist also alle Quellen und die Supersenke nimmt alles aus den Senken entgegen.
Die Knoten zwischen den Quellen und Senken haben dank der [[Flusserhaltungsbedingung]] automatisch einen Bedarf von Null.

Der Bedarf der Superquellen und Supersenken wird natürlich durch die Summe der Bedarfe der Quellen und Senken definiert.
![[Bildschirmfoto 2022-01-04 um 12.08.01.png]]

[[Minimalkosten-Zirkulations-Problem]]
