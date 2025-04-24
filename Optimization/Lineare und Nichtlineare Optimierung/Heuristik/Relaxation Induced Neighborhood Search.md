---
uni-module: "LNS"

alias: "RINS"
tags: Algorithmus
---

# Relaxation Induced Neighborhood Search

Häufig haben die [[Incumbent]] und [[LP-Relaxierung]] in großen Teilen der Variablen die gleichen Lösungswerte.

Wenn man diese Menge an Variablen fixiert wird ein neues Optimierungsproblem erzeugt, welches wahrscheinlich leichter gelöst werden kann.
Die Anzahl an Fixierungen sollte natürlich möglichst groß sein.
Außerdem wird dem Problem eine zusätzliche Ungleichung hinzugefügt um einen besseren ZFW zu erzwingen.

![[Bildschirmfoto 2022-07-14 um 15.32.10.png]]

## Arbeitsweise

![[Bildschirmfoto 2022-07-14 um 15.32.29.png]]
