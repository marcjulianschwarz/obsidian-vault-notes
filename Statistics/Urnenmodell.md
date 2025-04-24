---
uni-module: "StochMod"
---

# Urnenmodell

- $N$ Kugeln
- nummeriert durch $1, ..., N$
- man zieht $n$ Kugeln

Für die Anzahl der möglichen Resultate gibt es diese vier Modi:

|                  | mit Zurücklegen    | ohne Zurücklegen     |
| ---------------- | ------------------ | -------------------- |
| mit Reihenfolge  | $N^n$              |  $\frac{N!}{(N-n)!}$ |
| ohne Reihenfolge | $\binom{N+n-1}{n}$ | $\binom{N}{n}$       |

[[IMG - Urnenmodell Modi.png]]

## Weitere Urnenmodelle

[[Hypergeometrische Verteilung]]
[[Multinomialverteilung]]
[[Poisson Verteilung]]
[[Geometrische Verteilung]]
[[Negative Binomialverteilung]]
