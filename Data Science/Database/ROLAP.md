---
uni-module: KonzMod
---

# ROLAP

Eine Tabelle mit den Fremdschlüsseln der Dimensionen als Primärschlüssel und dem Fakt als Attribut.
-> Kann aufgeteilt werden in Struktur und Inhalt.

**Varianten**:
Star Schema -> Eine Tabelle für jede Dimension
Snow Flake Schema -> [[Normalisierung]] (eine Tabelle pro Klassifikationsstufe)

Die Fakten können als mehrstelliger Beziehungstyp (siehe [[ER-Modell]]) modelliert werden.

Beispiel Star Schema:
![[IMG - Star Schema.png]]

Beispiel Snow Flake Schema:
![[IMG - Snowflake Schema.png]]
