---
uni-module: StochMod
aliases:
  - Zufallsvariablen
  - Random Variable
  - Random Variables
  - Random Quantity
  - Aleatory Variable
  - Stochastic Variable
---

# Zufallsvariable

## Motivation

Manchmal ist man nicht unbedingt an einem bestimmten [[Ereignis]] interessiert sondern an einem Wert, der mit diesem [[Ereignis]] zusammenhängt.
Zum Beispiel möchte man bei einem _Dartwurf_ nicht wissen wie wahrscheinlich es ist eine bestimmte Koordinate zu treffen, sondern wie wahrscheinlich es ist in ein Feld (einer Menge an Koordinaten) zu treffen.

## Definition

Eine solche Abbildung aus dem [[Wahrscheinlichkeitsraum]] in einen anderen [[Wahrscheinlichkeitsraum]] nennt man Zuffalsvariable.
Dafür muss sie allerdings _messbar_ bezüglich der beiden [[Sigma Algebra | Sigma Algebren]] sein. Das heißt
$$X^{-1}(B) \in \mathcal{A}\quad \text{für alle}\quad B \in \mathcal{A}'$$

→ Eventuell ist es auch mal wichtig einen [[Messbarkeitsnachweis]] durchzuführen

## Verteilung

Zu dieser Abbildung ist dann auch eine [[Wahrscheinlichkeitsmaß|Verteilung]] $P_X$ definiert als
$$P_X(B) = P(X^{-1}(B))$$

## Stochastische Unabhängigkeit

Mehrere Zufallsvariablen sind [[stochastisch unabhängig]], wenn für alle [[Ereignis|Ereignisse]] aus der [[Sigma Algebra]] gilt, dass die [[gemeinsame Verteilung]] der Zufallsvariablen das gleiche ist wie das Produkt der einzelnen [[Wahrscheinlichkeitsmaß|Verteilungen]]

## Abbildung

![[IMG - Visualisierung Zufallsvariable mit Beispiel.png]]

## Beispiel

Ein Beispiel ist die [[Indikatorfunktion]]

## Kurzschreibweisen

![[IMG - Zufallsvariablen Verteilung Kurzschreibweisen.png]]

## Mehrere Zufallsvariablen

[[gemeinsame Verteilung]]
[[eindimensionale Randverteilung]]
![[IMG - Interpretation Unabhängigkeit von Zufallsvariablen mit gemeinsamer Verteilung.png]]
[[Binomialverteilung]]
