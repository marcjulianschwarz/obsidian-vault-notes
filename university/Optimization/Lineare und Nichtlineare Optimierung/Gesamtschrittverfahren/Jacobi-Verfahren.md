---
uni-module: "LNS"

tags: Algorithmus
alias: Gesamtschrittverfahren
---

# Jacobi-Verfahren

Kann zur Lösung [[Lineare Gleichungssysteme]] verwendet werden, die in [[Fixpunktform]] sind.

→ [[Umwandlung LGS in Fixpunktform]]

## Algorithmus

![[Bildschirmfoto 2022-05-13 um 11.32.07.png]]

## Konvergenz des Verfahrens

Es [[Konvergenz|konvergiert]] genau dann für jeden Startvektor gegen die Lösung, wenn der [[Spektralradius]] $< 1$ ist.

Wenn die [[Zeilensummennorm]] $<1$ ist hat das [[Lineares Gleichungssystem|LGS]] für jedes $u$ eine eindeutige Lösung und das [[Iterationsverfahren]]:

$$x^{(0)}$$
$$x^{(k+1)}=Tx^{(k)}+u$$
[[Konvergenz|konvergiert]] für jeden Startpunkt gegen diese Lösung.
→ Beweis: [[Fixpunktsatz von Banach]]

Das Jacobi-Verfahren [[Konvergenz|konvergiert]], wenn das [[Zeilensummenkriterium]] erfüllt ist.
