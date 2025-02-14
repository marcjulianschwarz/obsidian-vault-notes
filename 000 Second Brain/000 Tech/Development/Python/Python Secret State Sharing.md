Users will be able to use these methods as if they were independent but in reality they depend on the same instance (by the seed).

```python
from datetime import datetime

class Random8 (object) :
	def __init__(self):
		self.set_seed(datetime.now).microsecond % 255 + 1)

	def set_seed(self, value) :
		self.seed = value

	def random (self) :
		self.seed, carry = divmod (self.seed, 2)
		if carry:
			self.seed ^= 0xb8
		return self.seed

_instance = Random8 ()
random = _instance.random
set_seed = _instance.set_seed
```
