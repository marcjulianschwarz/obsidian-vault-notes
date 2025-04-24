---
uni-module: "StochMod"
---

# Hypergeometrische Verteilung

- [[Urnenmodell]]
- $M \leq N$ markierte Kugeln
- ziehen $n \leq N$ Kugeln ohne Zurücklegen und ohne Reihenfolge
- $A_k:=$ Unter den gezogenen Kugeln befinden sich genau $k$ markierte Kugeln
- $k \leq \min{(n, M)}$
- [[Laplace-Experiment]] [[Gleichverteilung]]
- [[Grundraum]] sind alle Teilmengen mit der Kardinalität $n$
- Die Karidnalität vom [[Grundraum]] ist $\binom{N}{n}$ [[Binomialkoeffizient]]
- Möglichkeiten $k$ markierte Kugeln zu ziehen: $\binom{M}{k}$
- Möglichkeiten $n-k$ unmarkierte Kugeln zu ziehen: $\binom{N-M}{n-k}$

$$h(k;n,N,M):=P(A_k)=\frac{\binom{M}{k}\cdot\binom{N-M}{n-k}}{\binom{N}{n}}$$
$$Hyp_{m,N,M}$$

Die hypergeometrische [[Wahrscheinlichkeitsmaß|Verteilung]] hat viele Anwendungen.
Im [[Asymptotisches Regime großer Gesamtheiten | asymptotischen Regime großer Gesamtheiten]] (also wenn $N$ gegen unendlich geht) steht sie mit der [[Binomialverteilung]] in Verbindung. Bei sehr großem $N$ spielt es eigentlich keine Rolle mehr ob man die Kugeln zurück in die Urne legt oder nicht. Die Wahrscheinlichkeit für eine markierte Kugel ist immer in etwa $\frac{N}{M}$

## Beweis, dass $h()$ im unendlichen die Binomialverteilung ist

![[IMG - Hypergeometrische Verteilung in großem Raum ist Binomialverteilung - Beweis.png]]
