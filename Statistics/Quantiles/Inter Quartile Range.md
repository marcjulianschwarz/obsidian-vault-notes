---
uni-module: "KDD"

alias: "IQR"
---

# Inter Quartile Range

The Inter Quartile Range can be calculated from the 75% and 25% [[Perzentil|Quartiles]] like this:
$$IQR=Q_3-Q_1$$

It is quite robust against [[Outlier]], just like the [[Median]].

## Python Implementation

```python
def remove_outliers(values, threshold=1.5)

	IQR = quantile75 - quantile25

	values = values >= quantile75 + 1.5 * IQR
	values = values <= quantile25 1.5 * IQR
	return values
```
