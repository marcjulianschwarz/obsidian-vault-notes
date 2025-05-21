---
uni-module: IDB

alias: [Abstrakte Maschine]
---

# Schicht

Eine Schicht realisiert einen bestimmten Dienst, den sie an die darüberliegende Schicht mittels einer Schnittstelle zur Verfügung stellt.
Dabei nimmt sie Dienste darunter in Anspruch und verbirgt sie damit auch [[Datenunabhängigkeit|Datenkapselung]].
Sie muss daher alle Funktionen anbieten.

Das Problem ist die passende Anzahl an Schichten zu finden. Bei sehr vielen Schichten kann der Koordinierungsaufwand zu groß werden. Normalerweise ist die Anzahl der Schichten zwischen 3 und 10.

Eine Schicht bezeichnet man auch als abstrakte oder virtuelle Maschine.

## Aufbau einer Schicht

Eine Schicht besteht aus einer Menge an Operationen, die an der Schnittstelle liegen.
Außerdem gibt es eine Menge an Datenobjekten (Adressierungseinheiten).
