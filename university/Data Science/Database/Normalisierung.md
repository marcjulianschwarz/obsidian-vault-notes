---
uni-module: "KonzMod"
---

# Normalisierung

## Warum?

[[ER-Mapping]] liefert keine Garantie für Redundanzfreiheit, denn schon das [[ER-Modell]] kann nicht korrekt erstellt sein (viele verschiedene Möglichkeiten).

Daraus resultieren verschiedene Anomalien:

1.  Einfüge Anomalie
2.  Lösch Anomalie
3.  Änderungs Anomalie

Mit Hilfe der Normalisierung wollen wir die Relationen in eine Form bringen, in welcher keine dieser Anomalien auftritt.

## Wie?

Durch Analyse der [[Funktionale Abhängigkeit]] zwischen Attributen. Je nachdem welche Abhängigkeiten gelten, könne Relationen in verschiedene Normalformen überführt werden.
Es ist aber wichtig, dass die Normalisierung eine abhängigkeitserhaltende und verlustfreie Zerlegung darstellt.

## Begriffe

-
- Superschlüssel: Alle Attribute sind vom Superschlüssel abhängig
- Schlüsselkandidat: Minimaler Superschlüssel
- Schlüsselattribut: Attribut eines Schlüsselkandidaten

## Normalformen:

- [[1. Normalform]]
- [[2. Normalform]]
- [[3. Normalform]]
- [[BCNF]]
- [[4. Normalform]]
- [[5. Normalform]]
- [[Denormalisierung]]
