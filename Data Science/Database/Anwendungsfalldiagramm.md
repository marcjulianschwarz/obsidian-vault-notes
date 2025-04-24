---
uni-module: "KonzMod"
---

# Use Case Diagramm

Ziel dieses Diagramms ist es ein System funktional zu beschreiben. Dabei werden Funktionen und Beziehungen unter diesen Funktionen modelliert. Zusätzlich gibt es Akteure, die außerhalb des Systems stehen und Funktionen des Systems benutzen können.
Mit einer Generalisierungsbeziehung lassen sich Unter und Oberklassen bilden. Außerdem gibt es abstrakte Anwendungsfälle, die so allerdings nicht ausgeführt werden, sondern nur Variationen davon.
Das Ziel dieses Diagramms ist es ein gemeinsames Verhalten wiederverwendbar zu machen.

![[Bildschirmfoto 2021-07-15 um 16.54.44.png]]

`<<include>>` -> Teilfunktion, die in anderen Funktionen auch benutzt wird (Dekomposition)
`<<extend>>` -> Variation des normalen Verhaltens (Ausnahmefälle)
