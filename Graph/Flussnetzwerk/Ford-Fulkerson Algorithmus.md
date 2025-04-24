---
uni-module: LKO
aliases:
  - Augmentierende-Wege-Algorithmus
tags:
  - Algorithmus
---

# Ford-Fulkerson Algorithmus

Bestimmt einen [[Maximaler Fluss | maximalen Fluss]].

![[Bildschirmfoto 2022-01-06 um 16.50.16.png]]

_Eingabe_: [[Flussnetzwerk]]
_Ausgabe_: [[Maximaler Fluss]], [[Minimaler Schnitt]]

Der minimale Schnitt ist ein Zertifikat, dass der Algorithmus richtig gerechnet hat, wenn dieser mit dem Wert des maximalen Flusses übereinstimmt.→ [[Max-Flow-Min-Cut-Theorem]]

## Optimalitätsbedingung

Ein wichtiger Baustein für die Optimalitätsbedingung ist das Konzept [[Augmentierender Weg]],denn ein Fluss $x$ ist genau dann maximal, wenn es keinen augmentierenden Weg bezüglich $x$ gibt.

## Per Hand anwenden

1. Flussnetzwerk mit leeren Kapazitäten aufschreiben
2. [[Residualnetzwerk]] aufstellen
   1. Pfad im Residualnetzwerk auswählen
   2. Residualkapazität des Pfades bestimmen
3. Flussnetzerk entsprechend dieser Kapazität anpassen
4. → 2. (bis man keinen Pfad mehr bilden kann)

→ Max-Flow ist erreicht
→ Min-Cut ist Schnitt zwischen allen Knoten, die durch einen Pfad noch erreicht werden können und denen, die nicht mehr erreicht werden können
