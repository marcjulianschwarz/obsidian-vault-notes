```python
from matplotlib.dates import DateFormatter
```

Rotating x-axis tick labels:
```python
ax.tick_params(axis="x", rotation=45)
```

Formatting x-axis tick labels if they are datetime objects:
```python
timeFmt = DateFormatter('%H:%M:%S')
ax.xaxis.set_major_formatter(timeFmt)
```

