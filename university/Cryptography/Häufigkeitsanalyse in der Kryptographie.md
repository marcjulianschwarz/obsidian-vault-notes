---
uni-module: "KRY"

alias: "Häufigkeitsanalyse"
---

# Häufigkeitsanalyse in der Kryptographie

Eine Häufigkeitsanalyse (zum Beispiel in Form eines [[Histogram]]) kann dazu verwendet werden um einzelne Buchstaben evenutell übersetzen zu können.
Eine einfache Tabelle zeigt für englische und deutsche Texte jeweils die Zeichenwahrscheinlichkeiten:

$$
\begin{array}{crr|crr}
\text { Zeichen } & \text { englisch } & \text { deutsch } & \text { Zeichen } & \text { englisch } & \text { deutsch } \\
\hline \text { A } & 8.04 & 6.47 & \mathrm{~N} & 7.09 & 9.84 \\
\mathrm{~B} & 1.54 & 1.93 & \mathrm{O} & 7.60 & 2.98 \\
\mathrm{C} & 3.06 & 2.68 & \mathrm{P} & 2.00 & 0.96 \\
\mathrm{D} & 3.99 & 4.83 & \mathrm{Q} & 0.11 & 0.02 \\
\mathrm{E} & 12.51 & 17.48 & \mathrm{R} & 6.12 & 7.54 \\
\mathrm{~F} & 2.30 & 1.65 & \mathrm{~S} & 6.54 & 6.83 \\
\mathrm{G} & 1.96 & 3.06 & \mathrm{~T} & 9.25 & 6.13 \\
\mathrm{H} & 5.49 & 4.23 & \mathrm{U} & 2.71 & 4.17 \\
\mathrm{I} & 7.26 & 7.73 & \mathrm{~V} & 0.99 & 0.94 \\
\mathrm{~J} & 0.16 & 0.27 & \mathrm{~W} & 1.92 & 1.48 \\
\mathrm{~K} & 0.67 & 1.46 & \mathrm{X} & 0.19 & 0.04 \\
\mathrm{~L} & 4.14 & 3.49 & \mathrm{Y} & 1.73 & 0.08 \\
\mathrm{M} & 2.53 & 2.58 & \mathrm{Z} & 0.09 & 1.14
\end{array}
$$

Durch die Analyse von Häufigkeiten von [[n-Gramm]] (wie Bigramm, Trigramme und Tetragramme) lassen sich noch weitere Buchstaben bestimmen.
