---
uni-module: "LNS"

tags: Algorithmus
---

# Gradientenverfahren

Das Gradientenverfahren verwendet als [[Abstiegsrichtung]] den negativen [[Gradient]] ([[Richtung des steilsten Abstiegs]]).

## Algorithmus

![[Bildschirmfoto 2022-05-31 um 23.07.00.png]]

[[Armijo-Schrittweitenregel]]

Abbruchbedingung in 2 wird meistens durch ein kleines $\epsilon$ als Toleranz ersetzt.

## Konvergenz

Verfahren [[Konvergenz|konvergiert]] entweder zu [[Stationärer Punkt]] oder erzeugt eine unendliche Folge für die gilt:

- Für alle $k$ gilt $f\left(x^{(k+1)}\right)<f\left(x^{(k)}\right)$
  - Es wird also bei jeder Iteration besser
- Jeder [[Häufungspunkt]] des Verfahrens ist [[Stationärer Punkt]] von $f$.

[[Rosenbrock-Funktion]]

_Beweis_: #todo, #uebung
