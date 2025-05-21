---
uni-module: LKO
---

# Konvexes Optimierungsproblem

Ein Optimierungsproblem ist ein konvexes Optimierungsproblem wenn sowohl $Z$ als auch die Zielfunktion [[Konvexe Menge|konvex]] sind.

Es sei also $f$ entsprechend eine stetige Zielfunktion, dann ist jede lokale Lösung auch eine globale Lösung.
Falls $f$ zusätzlich strikt konvex ist, besitzt das Problem höchstens eine globale Lösung.

Eine [[Konvexe Funktion]] ist auf einer [[Konvexe Menge]] definiert.

Falls eine Funktion nicht [[Stetigkeit|stetig]] ist so lässt sich trotzdem eine Art Ableitung bilden durch den [[Subgradient]] und das [[Subdifferential]].

Für ein Optimierungsproblem lässt sich die zulässige Menge an Punkten durch die Nebenbedingungen $h_j$ und $g_i$ darstellen als:
$$Z=\set{x\in\mathbb{R}:h_j(x)=0,g_i(x)\leq0}$$
Über diese Menge kann man Aussagen treffen:

1. sind $g_i$ und $h_j$ [[Stetigkeit|stetig]] so ist $Z$ abgeschlossen
2. sind $g_i$ [[Konvexe Menge|konvex]] und $h_j$ [[affin-linear]] so ist $Z$ konvex

Ob eine Funktion [[Konvexe Menge|konvex]] ist lässt sich mithilfe verschiedener Aussagen über die [[Definitheit]] der [[Hessematrix]] bestimmen. Wenn sie [[Definitheit|positiv semidefinit]] ist ist die Funktion konvex. Ist sie allerdings sogar [[Definitheit|positiv definit]], dann ist die Funktion auch strikt konvex.

[[Richtungsableitung]] wird definiert.

---

Wenn die Zielfunktion und die Lösungsmenge konvex ist, dann ist automatisch die lokale Lösung auch die globale Lösung.

- [[Konvexe Menge]]
- [[Konvexe Funktion]]

Es sei also $f$ entsprechend eine stetige Zielfunktion, dann ist jede lokale Lösung auch eine globale Lösung.
Falls $f$ zusätzlich strikt konvex ist, besitzt das Problem höchstens eine globale Lösung.
