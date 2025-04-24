---
uni-module: KRY
tags:
  - Algorithmus
---

# Fibonacci-Zahlen

[[Rekursion|Rekursiv]] definierte Folge an Zahlen mit
$$f_0 = 0$$
$$f_1=1$$
$$f_n=f_{n-1} + f_{n-2}$$

Man kann die $n$-te Fibonacci Zahl auch explizit berechnen mit
$$f_n=\frac{1}{\sqrt{5}}\left[\left(\frac{1+\sqrt{5}}{2}\right)^n-\left(\frac{1-\sqrt{5}}{2}\right)^n\right].$$
Außerdem gilt die Abschätzung
$$n \leq 4.785 \log _{10} f_{n+2}.$$

```python
def fibonacci_list(n):
	f = [0,1]
	while len(f) < n:
		f.append(f[-1] + f[-2])
	return f
```
