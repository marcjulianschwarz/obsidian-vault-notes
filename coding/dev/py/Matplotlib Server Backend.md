You might want to call:

```python
matplotlib.pyplot.switch_backend('Agg') 
```

so that your server does not try to create (and then destroy) GUI windows that will never be seen.