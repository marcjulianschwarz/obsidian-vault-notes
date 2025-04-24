---
uni-module: "KDD"
---

# Data Discretization

Can be used to turn numerical data into [[Categorical Data]] by creating intervals which replace the actual raw data values.

**Advantages are:**

- reduced data size
- can make some numerical attributes comparable

**Split (top-down) **

- split data into intervals which can be seen as one value

**Merge (bottom-up)**

- merge data until it becomes a "bigger chunk"

## Methods

- [[Binning]] → Unsupervised and top-down split
- [[Histogram Analysis]] → Unsupervised and top-down split
- [[Clustering]] → Unsupervised and top-down split or bottom-up merge
- Decision-tree analysis → Supervised and top-down split
- [[Correlation Analysis]] → e.g. [[Chi-Squared Test]] → Unsupervised and bottom-up merge
