---
uni-module: "LNS"

alias: "Natürliche Matrixnorm"
---

# Induzierte Matrixnorm

Die induzierte Matrixnorm mit $A$ quadratisch ist
$$||A||:=\operatorname{max}||Ax||$$ mit $$||x||=1$$
durch die [[Norm]] des [[Vektorräume und lineare Abbildungen|Vektorraum]] induziert.

Es gilt:
$$\|A\|=\max _{\|x\|=1}\|A x\|=\max _{x \neq 0}\left\|A \frac{x}{\|x\|}\right\|=\max _{x \neq 0} \frac{\|A x\|}{\|x\|}$$

→ #lnsexam diese Form kann wichtig für Beweise sein.

## Beispiel

![[Induzierte Matrixnorm 2022-07-10 18.16.28.excalidraw]]

## Eigenschaften

Induzierte Matrixnormen sind wegen den folgenden Eigenschaften besonders interessant und nützlich:

_Verträglichkeit mit der Vektornorm:_
$$||Ax||\leq ||A||\cdot||x||$$

_und Submultiplikativität:_
$$||AB||\leq ||A||\cdot ||B||$$
und [[Spektralradius]] $$\rho(A)\leq ||A||$$

## Beispiele

- [[Spektralnorm]]

_Related:_

- [[Maximumsnorm]]
