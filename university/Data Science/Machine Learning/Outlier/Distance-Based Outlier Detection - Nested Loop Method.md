---
uni-module: "KDD"
---

# Distance-Based Outlier Detection - Nested Loop Method

Formally:
$$\frac{\left\|\left\{\mathbf{o}^{\prime} \mid d\left(\mathbf{o}, \mathbf{o}^{\prime}\right) \leq r\right\}\right\|}{\|D\|} \leq \pi$$
where $o$ is an object from the [[Dataset]] $D$ and $r$ is the neighborhood around that object.

$\pi$ is a threshold that has to be determined.

We would call an [[Outlier]] a DB(r,$\pi$)-outlier.

Another way of formulating this would be to look at the $k$-nearest neighbor $o_{k}$ with $k=\lceil\pi n\rceil$.
$o$ would then be an outlier if the distance to $o_{k}$ is bigger than $r$.

[[Laufzeit]] $\mathcal{O}(n^{2})$ but linear in CPU time with respect to data set size, however it often terminates quickly with a small dataset that has few outliers.
Might be costly for large datasets that dont fit into [[RAM]].

Also objects are checked one by one and not group by group which slows down this algorithm.

Thus a better apporach is a **Grid-Based** method like the [[Distance-Based Outlier Detection - Grid-Based Method]].

## Simple Python Implementation

```python
def nested_loop_remove_outliers(data, pi, r):
    normal_data = []
    n = len(data)
    for oi in data:
        c = 0
        for oj in data:
            if oi != oj and abs(oi - oj) <= r:
                c += 1
                if c >= pi * n:
                    normal_data.append(oi)
                    break;
    return normal_data
```
