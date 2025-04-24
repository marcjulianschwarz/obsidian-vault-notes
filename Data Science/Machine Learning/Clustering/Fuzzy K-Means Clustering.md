---
uni-module: MBNN
---
# Fuzzy K-Means Clustering

Fuzzy [[k-means Clustering]] in contrast to normal [[Clustering]] will not find discrete centroids for each datapoint but rather a probability distribution over all clusters $u_{ij}$.

$$\sum_{j=1}^K \sum_{i=1}^N u_{i j}^f\left\|x_i-\mu_j\right\|^2 \rightarrow \min _{\mu_j, u_{i j}} \text { s.t. } \sum_{j=1}^K u_{i j}^f=1 \forall i$$

We can use the *fuzzifier* $f$ to control how discrete or not the clusters are.