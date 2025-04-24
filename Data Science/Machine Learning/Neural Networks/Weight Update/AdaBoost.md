---
uni-module: "KDD"

alias: "Adaptive Boosting"
---

# AdaBoost

A model based on [[Boosting]].

## Training

We have [[Dataset]] $D$ with samples $(x_{d},y_{d})$.

1. Initialize lists
   1. List to hold weights: $w$
   2. List to hold classifiers: $M$
   3. List to hold weight-updates: $\beta$
2. Initialize weigths for first classifier so that each tuple has the same probability. $w_{i}^1\leftarrow \frac{1}{d}$
3. Generate $k$ classifiers in $k$ iterations
4. At iteration $i$ do:
   1. Calculate normalized weights: $p^i=\frac{w^i}{\sum_{j=1}^N w_j^i}$
   2. Use [[Bootstap]] method to sample [[Dataset]] with replacement according to the previously assigned weights to form the training set $D_{i}$ for classifier $M_{i}$
   3. Derive model $M_{i}$ from $D_{i}$
   4. Test model $M_{i}$ with test set $D_{i}$ by calculating error $\epsilon_{i}$ as the sum of all missclassified weights $w_{i}$
   5. If this error is bigger than $0.5$ go back to step 4.1 and abandon this classifier
   6. Calculate the weight update $\beta_{i}$ as $\frac{\epsilon_{i}}{1-\epsilon_{i}}$
   7. Update weigths for the next iteration by multiplying them with $\beta_{i}$ if they have been correctly classified: $w_{i}^{i+1}=w_{j}^{i}\beta_{i}^{^-err(x_{j})}$ thus reducing the weight if they were classified correctly and leaving the weight as it is if it has been missclassified.
   8. Add $w^{i+1},M_{i},\beta_{i}$ to their respective lists

## Prediction

1. Initialize weigths of each class to zero
2. For each classifier
   1. Calculate weight of its vote: $w_{i}=\log\left( \frac{1}{\beta_{i}} \right)$
   2. Get prediction $c$ from that weak classifier
   3. Add $w_{i}$ to the weight for class $c$
3. Return class with the largest weight

Or in short:
$$M(x)=\arg \max _{y \in Y} \sum_{i=1}^k\left(\log \frac{1}{\beta_i}\right) M_i(x)$$
