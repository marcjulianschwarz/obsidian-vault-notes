---
uni-module: "KRY"

alias: "Monoalphabetische Substitutionschiffrierung"
---

# MASC-Verschlüsselung

Ein monoalphabetisches [[Substitutionsverfahren]]:

> [!TIP] [[Alphabet]] > $A,\dots, Z$ identifiziert mit den Zahlen $0,\dots,25$

> [!Tip] [[Schlüssel]]
> Wort $K$

**Verfahren:**

1. Mehrfach vorkommende Buchstaben aus Schlüsselwort entfernen
2. An das Schlüsselwort wird das zyklisch permutierte Alphabet angehängt, wobei mit dem Buchstaben begonnen wird, der nach dem letzten Buchstaben des Schlüsselwortes kommt

Mit diesem Verfahren ergeben sich $26!$ mögliche Permutationen.

Die [[CAESER Verschlüsselung]] ist ein Spezialfall der MASC-Verschlüsselung wobei das Schlüsselwort aus genau einem Buchstaben besteht.

## Beispiel

Schlüssel: ERLANGEN

1. ERLANG
2. HIJKMOPQSTUVWXYZBCDF
