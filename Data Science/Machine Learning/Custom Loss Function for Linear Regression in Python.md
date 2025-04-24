 
# Custom Loss Function for Linear Regression in Python

```python
from scipy.optimize import minimize

def error(y_true, y_pred):
	...

def loss(params, x, y_true):
	pred = ...params...
	return ...loss(y_true, pred)...

d = minimize(loss, [0,1], args=(x, y_true))
res = d.x
```

## Source 
- https://alex.miller.im/posts/linear-model-custom-loss-function-regularization-python/
