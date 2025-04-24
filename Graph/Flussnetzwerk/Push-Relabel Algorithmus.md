---
uni-module: "LKO"

alias: ["Preflow-Push"]
tags: "Algorithmus"
---

# Push-Relabel Algorithmus

Sind [[Dualität|dual]] zu AW-Algorithmen.

## Idee

So viel [[Fluss]] wie möglich auf das [[Flussnetzwerk]] schicken. Dabei darf die [[Flusserhaltungsbedingung]] verletzt werden.
Durch die Verletzung entsteht ein [[Überschuss]], der in einem [[Pseudofluss]] aber erlaubt ist.

## Wofür

Zur Vermeidung vieler [[Augmentierender Weg | Augmentierender Wege]] wie in diesem Fall:
![[Bildschirmfoto 2022-01-03 um 12.59.44.png]]

[[Gültige Markierung]]
(Nicht-)Saturierte Schübe

Ein Algorithmus, der dieses Konzept verwendet ist der [[Goldberg–Tarjan Algorithmus]].
