---
uni-module: "KDD"
---
# Decision Tree

A [[Supervised Learning]] method that can be used both for [[Classification]] and [[Regression]] tasks. A decision tree can be created by [[Decision Tree Induction]]. 

**Prediction**
For [[Regression]] the prediction is the [[Arithmetic Mean|Mean]] outcome value of all instances in the reached leaf node.

## Components

- Root
- Internal nodes labeled by attributes 
- Leaf nodes labeled by classifications
- Branches correspond to attribute values 

## Regularisation 

A method of [[Regularisation]] is [[Decision Tree Pruning]].


## Scalable Decision Trees 

- [[RainForest]]
- [[BOAT]]

## Explainability

- Feature importance: go through all nodes of a feature to sum (and scale) how much the variance (or Gini index in case of classification) was reduced by that node (global)
- Explain individual predictions by a sum of split contributions, which is rewritten as a sum of feature contributions: (local)

$$\hat{f}(x)=\bar{y}+\sum_{d=1}^D \text { split.contrib }(\mathrm{d}, \mathrm{x})=\bar{y}+\sum_{j=1}^p \text { feat.contrib }(\mathrm{j}, \mathrm{x})$$

> [!Note]+ Quality of Explanations
>
> - highly [[Contrastive]]
>   - one can think about alternative routes through the tree
> - medium [[Fidelity]]
>   - struggle with linear relationships
>   - feature interactions are automatically captured
>   - lack of smoothness
> - medium [[Selectivity]]
>   - good explanations as long as they are short
>   - tune with hyperparameters such as max tree depth, min impurity
>   - but hurts [[Accuracy]]
> - low [[Stability]]
>   - slight change in features can create completely different tree and therefore different explanations

## Rules 

[[IF-THEN Rules for Classification]]

[[Rule Extraction from Decision Tree]]
[[Rule Induction]]
[[Rule Pruning]]

## Example

![[Bildschirmfoto 2022-06-20 um 15.39.05.png]]

## Further references

- https://www.inf.unibz.it/~mkacimi/lecture5.pdf
- https://www3.cs.stonybrook.edu/~cse352/L8DTIntro.pdf
