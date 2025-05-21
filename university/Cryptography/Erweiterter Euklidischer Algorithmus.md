---
uni-module: KRY
tags:
  - Algorithmus
---

# Erweiterter Euklidischer Algorithmus

Ein [[Algorithmus]] um die Gleichung ([[Satz von Bezout]])

$$ggT(a,b)=xa+yb$$
zu lösen. Das kann später auch dafür verwendet werden um die Gleichung
$$ax+by=c$$ zu lösen.

## Variante 1

Wir können das Schema des [[Euklidischer Algorithmus|euklidischen Algorithmus]] verwenden um $a_n=ggT(a, b)$ als [[Linearkombination]] von $a_0=a$ und $a_1=b$ zu schreiben.
Dabei eliminieren wir $a_n$ sukzessiv.
Systematisch lässt sich das Vorgehen als folgendes Schema darstellen:

![[Bildschirm­foto 2023-02-14 um 22.35.20.png]]

Zusammengefasst als:

![[Bildschirm­foto 2023-02-25 um 22.09.32.png]]

```python
def eea(a, b):
	"""first variant of eea
	"""
	q = []
	a = [a, b]
	x = [1, 0]
	y = [0, 1]
	while a[-1] > 0:
		q = a[-2] // a [-1]
		a.append(a[-2] - q*a[-1])
		x.append(x[-2] - q*x[-1])
		y.append(y[-2] - q*y[-2])
	return a[-2], x[-2], y[-2]
```

## Variante 2

Hier verzicht auf merken der Folgen $a_i,x_i,y_i$.

```python
def eea(a, b):
	"""second variant of eea
	"""
	x, y = 1, 0
	xx, yy = 0, 1
	while b > 0:
		q = a // b
		a, b = b, a - q*b # same as a % b
		x, xx = xx, x - q*xx
		y, yy = yy, y - q*yy
	return a, x, y
```
