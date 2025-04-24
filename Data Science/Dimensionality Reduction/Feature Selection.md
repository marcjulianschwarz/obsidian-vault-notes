---
uni-module: "KDD"

alias: "Attribute Subset Selection"
---

# Feature Selection

A way to reduce the dimensionality of a [[Dataset]].

## Methods

- Remove redundant attributes or irrelevant attributes (e.g. IDs)
  - manul selection with expert knowledge
- [[Heuristic Search]]

- [[Lasso Regression|LASSO]]
- [[Elastic-Net Regression]]
- [[Sensitivity Analysis]]

- Univariate selection by [[Korrelation|Correlation]] coefficient between feature and target (minimum threshold to keep feature)
  - might miss other interactions
- Forward Selection
  - train with one feature, select the best feature
  - add feature
  - repeat until number of desired features is reached
- Backward Selection
  - start with all features
  - remove one feature, throw away with best performance
  - repeat
