---
uni-module: "KDD"
---

# Correlation Analysis

## Numerical data

→ [[Korrelation|Correlation]], [[Kovarianz|Covariance]], [[Sample Covariance]], [[Varianz|Variance]]
→ Visual detection using [[Scatter Plot]] or [[Scatter Plot Matrices]].

## Nominal data

X = set of all distinct combinations of attributes
Y = set of all tuples

Actual quantity:
$$c_{i j}=\#\left\{(a, b) \in Y \mid a=a_{i}, b=b_{i}\right\}=Y\left(\left(a_{i}, b_{j}\right)\right)$$

Expected quantity in case of independence:
$$e_{i j}=\frac{\sum_{k=1}^{m} c_{i k}}{\# Y} \cdot \frac{\sum_{l=1}^{n} c_{l j}}{\# Y} \cdot \# Y=\frac{\sum_{k=1}^{m} c_{i k} \cdot \sum_{l=1}^{n} c_{l j}}{\# Y}$$

$$\sum_{k=1}^{m} e_{i k}=\sum_{k=1}^{m} c_{i k} \text { and } \sum_{l=1}^{n} e_{l j}=\sum_{l=1}^{n} c_{l j}$$

![[Bildschirmfoto 2022-05-11 um 21.51.47.png]]

To determine [[Korrelation|Correlation]] you need to apply the [[Chi-Squared Test]] to the values in the table.

## Python Implementation

```python
def correlation(AS: pd.Series, BS: pd.Series):
    A = AS.unique()
    B = BS.unique()
    A = np.flip(A)
    B = np.flip(B)

    n = len(A)
    m = len(B)

    # Generate all possible combinations of values in A and B
    X = [(i, j) for i in A for j in B]
    Y = [(i, j) for i, j in zip(AS,BS)]

    nY = len(Y)

    def actual(i, j):
        count = 0
        for ab in Y:
            if ab[0] == i and ab[1] == j:
                count = count + 1
        return count

    def expected(i, j):
        s1 = sum([actual(i, k) for k in B])
        s2 = sum([actual(l, j) for l in A])
        return (s1 * s2) / nY

    # Calculate Expected and Actual matrices
    e_table = np.zeros((m,n))
    c_table = np.zeros((m,n))
    for i, b in enumerate(B):
        for j, a in enumerate(A):
            c = actual(a, b)
            e = expected(a, b)
            e_table[i, j] = e
            c_table[i, j] = c

    # Calculate Chi Squared Value
    chi = 0
    for i in range(n):
        for j in range(m):
            e = e_table[i, j]
            c = c_table[i, j]
            chi += (c - e)**2 / (e)

    return c_table, e_table, chi
```
