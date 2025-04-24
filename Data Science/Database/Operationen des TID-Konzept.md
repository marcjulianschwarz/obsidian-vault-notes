---
uni-module: IDB
---

# Operationen des TID-Konzept

## Löschen

1. Der Eintrag im [[Positionsindex]] wird als ungültig markiert
2. Ander Sätze können verschoben werden um den Platz zu maximieren (es ändern sich nur die Einträge im [[Positionsindex]] und nicht die [[Satzadresse]])

## Änderungsoperation

- Länge darf sich ändern
- Wenn Länge für den [[Block]] zu groß wird, dann wird der [[Satz]] in den nächsten [[Block]] verschoben
- Bei Verschiebung wird einfach statt dem [[Satz]] die neue TID hingeschrieben. Heißt, auch hier ändert sich die ursprüngliche TID nicht. Man geht mehr oder weniger einfach diese Kette entlang.

![[IMG - Verschiebung Satz.png]]
