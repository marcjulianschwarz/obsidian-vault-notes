```python
import string 
import random 

alphabet = string.ascii_uppercase + string.ascii_lowercase + string.digits

def random_choice():
    return ''.join(random.choices(alphabet, k=8))
```

This is fast but of course like with all IDs you have to check for collisions.
