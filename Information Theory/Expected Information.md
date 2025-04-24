---
uni-module: KDD
aliases:
  - Entropy
---
# Expected Information

$$\operatorname{Info}(D)=-\sum_{i=1}^{m} p_{i} \log _{2}\left(p_{i}\right)$$

where $p_i$ is the probability that [[Entity|tuple]] in $D$ belongs to class $C_i$ which can be estimated by $\frac{|C_i|}{|D|}$.
The [[Erwartungswert|Expectation]] of [[Surprisal]] over every possible outome.


It is used to calculate [[Information Gain]] and [[Perplexity]].

## Python Implementation

```python
def information(dataset: pd.DataFrame, target_attribute: str) -> float:
	p = dataset.value_counts(target_attribute) / dataset.shape[0]
	return -sum([pi * log(pi, 2) for pi in p])
```
