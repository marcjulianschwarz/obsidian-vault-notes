---
uni-module: "LKO"

tags: Algorithmus
---

# Bellmann-Ford Algorithmus

Ist ein _Kürzeste Wege Algorithmus_, der von einem Startknoten $s$ aus die kürzesten Wege zu allen anderen Knoten berechnet. Dabei dürfen die Kantengewichte beliebig sein (also auch negativ). Allerdings darf es **keinen** negativen [[Zyklus]] bzw [[Kreis]] geben.

![[Bildschirmfoto 2022-01-06 um 16.44.53.png]]

### [[Laufzeit]]

ist $\mathcal{O}(n\cdot m)$.
Will man die kürzesten Wege von jedem Knoten aus zu jedem anderen Knoten haben ist die Laufzeit entsprechen $\mathcal{O}(n^2\cdot m)$#
