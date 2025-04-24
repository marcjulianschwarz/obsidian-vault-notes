---
uni-module: "LKO"

tags: "Algorithmus"
---

# Quick Sort

![[Bildschirmfoto 2022-01-06 um 16.05.13.png]]

### [[Python]] Implementierung

```python
def quick_sort(a, l, r):
	i = l
	j = r

	while i < j:
		while a[i] <= a[r] && i < j:
			i = i + 1
		while a[j] >= a[r] && i < j:
			j = j - 1

		a[i], a[j] = a[j], a[i]

		if l < i - 1:
			quick_sort(a, l, i-1)
		if i + 1 < r:
			quick_sort(a, i+1, r)
	return a
```

### [[Laufzeit]]

Durchschnitt: $\mathcal{O}(n\log{n})$
Worst-Case: $\mathcal{O}(n^2)$

→ Noch schneller im Worst-Case ist der [[Heap Sort]]
