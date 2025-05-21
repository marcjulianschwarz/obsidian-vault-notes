---
uni-module: "LNS"
---

# Umwandlung LGS in Fixpunktform

[[Lineares Gleichungssystem|LGS]] → [[Fixpunktform]]

$Ax=b$ mit $A$ quadratisch

Dann lässt sich $A$ darstellen als
$$A=L+D+U$$
wobei $D$ die Diagonale und $L,U$ jeweils das linke untere beziehungsweise rechte obere Dreieck von $A$ sind.
Wenn $A$ regulär ist so lässt sich $D$ invertieren. _Beweis_: Permutationsmatrix → alle Diagonalelemente rekursiv auf Nicht-Null Einträge bringen.

$$(L+D+U)x=b$$
$$Dx=-(L+U)x+b$$
$$x=-D^{-1}(L+U)x+D^{-1}b$$
die Iterationsmatrix ist hier $T_G=-D^{-1}(L+U)$
