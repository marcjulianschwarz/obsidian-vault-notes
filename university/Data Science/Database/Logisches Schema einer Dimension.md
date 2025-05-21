---
uni-module: "KonzMod"
---

# Logisches Schema einer Dimension

Partiell geordnete Menge von Klassifikationsstufen, die auch parallel verlaufen dürfen. Die verschiedenen Klassifikationsstufen stehen immer in einer 1:N Beziehung.
Zwischen verschiedenen Dimensionen existieren keine Beziehungen, denn Dimensionen sollten immer unabhängig voneinander sein.

![[IMG - Dimensionenmodell.png]]

Funktionale Abhängigkeiten im Logischen Schema -> Baumstruktur als Instanz.
Jeder Pfad in dem Schema ist eine Klassenhierarchie und wird als Baum dargestellt.
Eine Dimension sind also alle Klassenhierarchien zusammen.
