---
uni-module: "LKO"

tags: "Algorithmus"
---

# Selection Sort

![[Bildschirmfoto 2022-01-06 um 16.01.33.png]]

### [[Python]] Implementierung

```python
def selection_sort(a):
	for i in range(1, a.length):
		min = i
		for j in ragne(i+1, a.length):
			if a[j] < a[min]:
				min = j
		a[min], a[i] = a[i], a[min]
	return a
```

### [[Laufzeit]]
