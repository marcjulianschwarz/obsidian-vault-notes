---
uni-module: "KRY"
---

# PLAYFAIR-Verschlüsselung

- [[Alphabet]]: 25 von J verschiedene Buchstaben (ersetzte J durch I).
- [[Schlüssel]]: Wort, das in 5x5 Matrix zeilenweise geschrieben wird, Rest aufgefüllt mit restlichem Alphabet

**Verschlüsselung**

1. Aufteilen des Textes in 2er Blöcke
   1. Einsetzten von X, damit alle Blöcke immer aus zwei verschiedenen Buchstaben bestehen
2. Ein Block ist jetzt gegeben mit Buchstabe A und B
   1. Zeile A = Zeile B
      1. Beide verschieben um eine Spalte nach rechts
   2. Spalte A = Spalte B
      1. Beide verschieben um eine Zeile nach unten
   3. Spalte und Zeile unterschiedliche
      1. Vertausche die Spalten

**Entschlüsselung**

1. Aufteilen des Textes in 2er Blöcke
   1. Einsetzten von X, damit alle Blöcke immer aus zwei verschiedenen Buchstaben bestehen
2. Ein Block ist jetzt gegeben mit Buchstabe A und B
   1. Zeile A = Zeile B
      1. Beide verschieben um eine Spalte nach links
   2. Spalte A = Spalte B
      1. Beide verschieben um eine Zeile nach oben
   3. Spalte und Zeile unterschiedliche
      1. Vertausche die Spalten
