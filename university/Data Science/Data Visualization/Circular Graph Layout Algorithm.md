---
uni-module: "InfoVis"
---

# Circular Graph Layout Algorithm

1. Sort nodes with respect to [[Community Structure]] (groups)
2. Sort nodes inside of groups based on [[Graph Centrality]]
3. Size of node is given by the angle.
   1. Mapping from centrality to angle ($[0,s]\rightarrow[0,2\pi]$)
4. Position Node
   1. $x=R\operatorname{cos}(\alpha)$
   2. $y=R\operatorname{sin}(\alpha)$
   3. Advance by $\frac{\alpha}{a}+\frac{\beta}{2}$
5. Node Radius
   1. $r=R\operatorname{sin}(\frac{\alpha}{2})$

## Visually

![[Bildschirmfoto 2022-09-01 um 13.25.51.png]]
![[Bildschirmfoto 2022-09-01 um 13.25.59.png]]![[Bildschirmfoto 2022-09-01 um 13.26.07.png]]
