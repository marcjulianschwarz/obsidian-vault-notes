---
uni-module: "KRY"
---

# Kasiski-Test

1. Finde kurze Zeichenketten $b_{i}$ und $b_{j}$, die mehrfach auftreten
2. Die Länge des Schlüssels $n$ ist also ein Teiler der Differenz $j-i$
3. Es kann also passieren, dass
   1. $n \mid \operatorname{ggT}\left(j_1-i_1, j_2-i_2, j_3-i_3, \ldots\right)$
   2. oder $n=\operatorname{ggT}\left(j_1-i_1, j_2-i_2, j_3-i_3, \ldots\right)$
4. Der Chiffretext wird zeilenweise in eine Tabelle mit $n$ Spalten eingetragen
5. Die einzelnen Spalten sind nun $k_{i}$ [[CAESER Verschlüsselung|CAESER]] verschlüsselt.
6. Durch Häufigkeitsanalyse (Buchstabe E) können die einzelnen Spalten entschlüsselt werden
