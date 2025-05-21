---
uni-module: "InfoVis"
---

# Network Distance Statistics

Distance between nodes is the shortest [[Weg|Path]] between them.

Can be used to measure node importance or analyze the structure of a [[Graph]].

- [[Eccentricity]]
- [[Radius of a Graph]]
- [[Diameter of a Graph]]

These measures can be used to discriminate among different networks:

Average Length of Shortest Paths:
$$\bar{d}(u)=\frac{1}{|V|-1} \sum_{v \in V(G), v \neq u} d(u, v)$$
Average Path Length:
$$\bar{d}(G)=\frac{1}{|V|} \sum_{u \in V} \bar{d}(u)$$
Characteristic Path Length ([[Median]]):
$$\operatorname{median}\{\bar{d}(u) \mid u \in V(G)\}$$
