---
uni-module: "LKO"

tags: "Algorithmus"
---

# Goldberg–Tarjan Algorithmus

Ist ein [[Push-Relabel Algorithmus]].

![[Bildschirmfoto 2022-01-03 um 12.58.48.png]]

In Schritt 1 werden der Fluss und die [[Gültige Markierung]] initialisiert.

Der Algorithmus terminiert in Schritt 2 erst dann, wenn es keine aktiven Knoten mehr gibt ([[Überschuss]] ist überall gleich Null) und somit ein gültiger [[Fluss]] entstanden ist.

In Schritt 3 darf irgendein aktiver Knoten gewählt werden, bei dem der [[Überschuss]] abgebaut werden muss.

Falls es in Schritt 4 einen zulässigen Bogen gibt, auf den man $\delta$ schicken kann, so wird das gemacht. $\delta$ ist entweder der [[Überschuss]] selbst, wenn die [[Kapazitätsbedingung]] das zulässt. Ansonsten wird die Residualkapazität verwendet.
Falls in Schritt 4 allerdings kein zulässiger Bogen mehr existiert wird der restliche [[Überschuss]] durch eine Relabel-Operation über den nächstbesten Knoten geschickt.

## [[Laufzeit]]

Der Algorithmus führt maximal $\mathcal{O}(n^2)$ Relabel-Operationen und $\mathcal{O}(n^2m)$ Push-Operationen durch.

Mit geeigneten Datenstrukturen kann die Laufzeit auf $\mathcal{O}(n^2m)$ reduziert werden.
