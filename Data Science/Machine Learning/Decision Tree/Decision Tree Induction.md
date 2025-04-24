---
uni-module: KDD
aliases:
  - DTI
  - Decision Tree Learning
  - DTL
---
# Decision Tree Induction

Learning process of a [[Decision Tree]].

The simplest (and trivial) decision tree would be to have a path for each input example to a leaf node. This would perfectly realize the targets but would not generalize well on unseen data.
Instead we prefer to find more **compact** trees by only looking at attributes that are the most important for deciding on the target value. 

- Use an [[Attribute Selection Method]] to select an attribute that is best for splitting the tree into new branches
- Split the Tree
	- Use the new subtrees to repeat the steps
- Stop when
	- all tuples belong to the same class
	- all attributes have been used for splitting
	- no tuples has to be classified anymore
	- max node depth is reached
	- minimum number of instances in current node is reached
	- minimum impurity in current node is reached

[[Classification and Regression Trees|CART]]

![[CleanShot 2023-09-30 at 11.31.31@2x.png]]