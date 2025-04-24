---
uni-module: "KDD"

alias: ["Gini Coefficient", "CART", "IBM IntelligentMiner"]
---

# Gini Index

Measures statistical dispersion.

0 → perfect equality, all values same class
1 → maximum ineuqality

Based on [[Lorenz Curve]].

$$\operatorname{Gini}(D)=1-\sum_{j=1}^{n} p_{j}^{2}$$

$$\Delta \operatorname{Gini}_{A}(D)=\operatorname{Gini}(D)-\operatorname{Gini}_{A}(D)$$

Attribute with minimum Ginig Index is used.

## Example

![[Bildschirmfoto 2022-06-20 um 18.22.24.png]]

## Disadvantages

- Biased to multi-valued attributes
- Has difficulties when number of classes is large
- Tends to favor equal-sized partitions and purity in both of them
