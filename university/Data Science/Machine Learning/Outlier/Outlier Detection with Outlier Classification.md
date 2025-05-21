---
uni-module: "KDD"
---

# Outlier Classification

## [[Supervised Learning]]

- Samples were labeled by domain experts.
- Model normal objects and report those not matching the model as [[Outlier|Outliers]]
- Model [[Outlier|Outliers]] and treat those not matching the model as normal

Challenges are:

- Imbalanced classes
  - boost outlier class by [[Oversampling]] and maybe [[Undersampling]] of normal objects
- catch as many outliers as possible
  - [[Recall]] is more important than [[Accuracy]]

## [[Unsupervised Learning]]

- No labels available
- Use [[Clustering]] method to cluster data
  - samples not falling in any cluster are outliers

Challenges are:

- Samples outside of clusters might not be outliers
- Costly
- Hard to distinguish from noise
- cant detect collective outliers as they will most likely be treated as just another cluster

## [[Semi-Supervised Learning]]

- only few labels available
- if some normal objects are labeled
  - use these and the proximate ulabeled object to train a model for normal objects
  - report non fitting objects as outliers
- if some outlier objects are labeled
  - may not cover all possible types of outliers
  - thus use models from [[Unsupervised Learning]] to help recognize normal objects
