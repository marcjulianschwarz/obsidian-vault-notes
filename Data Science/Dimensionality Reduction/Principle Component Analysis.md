---
uni-module: EMD

alias: "PCA"
---
# Principal Component Analysis

PCA is a method to reduce the dimensions of a [[Dataset]] while keeping most information. We do this by rotating the [[Dataset]] and projecting the points to one (or $n$) dimensions.

To preserve distances and therefore information, you need to find the dimensions with highest [[Varianz|Variance]] while discarding the ones with lowest variance.

> [!Check]- Applications 
> - image (data) compression
> - facial recognition with eigenfaces
> - anomaly detection (first k components show normal behaviour)
> 

**Limitation**: Adidas Problem

## How to calculate

$X$ is the input matrix with $n$ datapoints and $p$ features.

Optional but recommended:
- standardize values (e.g. [[Z-score]])

- Calculate [[Eigenwert|Eigenvalues]] and [[Eigenvektor|Eigenvectors]] of $X$
	- [[Kovarianz|Covariance]] matrix $C=XX^T$
	- $C = WLW^T$ where $W$ are the eigenvectors and $L$ are the eigenvalues on the diagonal in decreasing order 
- Alternatively perform a [[Singular Value Decomposition]].
	- unitary matrix $U$
	- matrix $S$ with singular values on the diagonal
	- matrix $W$ with the singular vectors 
	- $X = USW^T$

Inserting this into the covariance matrix will get us: $WS^2W^T$" where the eigenvalues correspond to the squared singular values and the eigenvectors to the singular vectors.

Finally we can project the data with 
$$T = XW.$$
We then only want to keep the $q$ most important dimensions determined by the order of the $\lambda_i$.

## Assess feature contributions

See [[Loading]].
