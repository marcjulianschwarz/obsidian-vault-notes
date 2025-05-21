---
uni-module: KRY
tags:
  - Algorithmus
---
# Euklidischer Algorithmus

## Variante 1

Wir beginnen mit $a_0=a$ und $a_1=b$.

![[Bildschirm­foto 2023-02-25 um 21.57.26.png]]

## Variante 2

```python
def ggT(a, b):
	a = [a, b]
	while a[-1] > 0:
		a.append(a[-2] % a[-1])
	return a[-2]
```

## Variante 3

Ohne explizites merken der Zahlen in $a$.

```python
def ggT(a, b):
	while b > 0:
		a, b = b, a % b
	return a
```

## [[Laufzeit]]

Die [[Laufzeit]] des Algorithmus lässt sich mit den [[Fibonacci-Zahlen]] gut in Abhängigkeit von $a$ abschätzen.

Dafür sei $n$ die Zahl an Schritten, die wir abschätzen wollen.

Wir verwenden das [[Rekursion|rekursive]] Schema des Algorithmus wobei wir die $a=g_{n+1}$ und $b=g_n$ setzen. Führen wir damit das ganze Schema durch erhalten wir zum Schluss $ggT(a,b)=g_1$.
Wir können nun die Folge $g_n$ mit den [[Fibonacci-Zahlen]] vergleichen und sehen, dass diese immer größer gleich sind:
$$a=g_{n+1}\geq f_{n+2}.$$
Da wir $f_{n+2}$ bereits gut abschätzen können, lässt sich das ganze auch für $a$ abschätzen. Wir erhalten also:

$$n \leq 4.785 \log _{10} f_{n+2} \leq 4.785 \log _{10} a.$$
Der [[Algorithmus]] ist also sehr effizient und schnell.
