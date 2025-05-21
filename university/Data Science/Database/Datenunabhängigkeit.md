---
uni-module: ["KonzMod", "IDB"]

alias: [Datenabstraktion, Datenkapselung]
---

# Datenunabhängigkeit

Das _Speichern und Wiedergewinnen_ von Daten ohne Kenntnisse über die Speicherung der Daten.
Also es sollten keine Speicheradressen offen liegen oder Bytefolgen zu verwenden. Stattdessen werden Namen und Typen verwendet.
Außerdem sollen die Daten persistent gespeichert werden, also über das Programmende hinaus.
Zuletzt müssen Daten wiedergewonnen werden, also durch Suchen oder durch Übergeben.

## KonzMod

Das [[Konzeptionelles Schema | Konzeptionelle Schema]] muss so aufgebaut sein, dass Anwendungen unabhänig von den Daten sind. Das heißt es darf zu keinen Problemen führen, wenn sich zum Beispiel Speicherungsstrukturen verändern. Das wird normalerweise durch das [[Internes Schema | Interne Schema]] garantiert.
