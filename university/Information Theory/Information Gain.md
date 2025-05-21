---
uni-module: "KDD"

alias: "ID3"
---

# Information Gain

An [[Attribute Selection Method]] which selects the attribute with the highest **information gain**.

$$\operatorname{Gain}(A)=\operatorname{Info}(D)-\operatorname{Info}_A(D)$$
where $\text{Info}$ is the [[Expected Information]] also called [[Expected Information|Entropy]]. 

So for a [[Binary Classification]] we have 
$$\operatorname{Gain}(A)=I\left(\left\langle\frac{p}{p+n}, \frac{n}{p+n}\right\rangle\right)-\sum_a \frac{p_a+n_a}{p+n} I\left(\left\langle\frac{p_a}{p_a+n_a}, \frac{n_a}{p_a+n_a}\right\rangle\right)$$

Calculate [[Expected Information]] for every attribute and data partition.

```python
def information_partitioned(dataset: pd.DataFrame, target_attribute: str, partition_attribute: str) -> float:

    weights = dataset.value_counts(partition_attribute) / dataset.shape[0]
    return sum(
        [
	        weight * information(
	            dataset[dataset[partition_attribute] == index],
	            target_attribute
            )
	        for index, weight in weights.items()
        ]
    )
```

→ See [[Expected Information]] for `information()`

```python
def information_gain(dataset: pd.DataFrame, target_attribute: str, partition_attribute: str) -> float:

    return information(dataset, target_attribute) - information_partitioned(dataset, target_attribute, partition_attribute)
```


Select attribute with the highest gain first.

## Disadvantages

- Biased towards multi-valued attributes
- favors attributes with large numbers
