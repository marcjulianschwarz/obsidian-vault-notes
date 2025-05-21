---
uni-module: "AI"
---
# Decision Network

A decision network is a [[Bayesian Network]] with added action nodes and utility nodes (also called value node) that enable decision making.

Here, the treatment is an action node and U is the utility node.

![[CleanShot 2023-09-28 at 10.54.29@2x.png]]

## Construction 

1. Create a causal model, a [[Graph]] with nodes for symptoms, disorders, treatments, outcomes and their influences 
2. Simplify by removing [[Zufallsvariable|Random Variables]] that are not involved in the treatment decision 
3. Assign probabilities to the CPTs via patient databases, literatur studies or experts knowledge. This makes it a [[Bayesian Network]]
4. Assign utilities in the form of QALYs or Micromorts
5. Verify and refine the model by e.g. running the model backwards an comparing the values with the literature 
6. Perform a [[Sensitivity Analysis]] to see whether the optimal decision is robust against changes in the parameters 

