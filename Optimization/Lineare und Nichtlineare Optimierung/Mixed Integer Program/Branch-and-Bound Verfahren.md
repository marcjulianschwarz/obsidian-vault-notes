---
uni-module: "LNS"

tags: Algorithmus
---

# Branch-and-Bound Verfahren

Das [[Branch-and-Bound Verfahren]] nutzt eine [[Relaxierung]], die [[LP-Relaxierung]], aus um ein [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] zu vereinfachen, indem es in Teilprobleme aufgespalten (Branch) wird.

Dabei verwendet es verschiedene Bedingungen (Bound) um nicht alle möglichen Teilprobleme lösen zu müssen:
- [[Prune by Infeasibility]]
- [[Prune by Integrality]]
- [[Prune by Bound]]


Ein Verfahren zum lösen von Gemischt-ganzzahligen linearen Optimierungsproblemen.

_Für das Problem lässt sich der ZFW beschränken:_

- $\hat{z}$ → Wert einer Optimallösung $\hat{x}$ von [[Lineares Optimierungsproblem|LP]]
- $z^*$ → Wert einer Optimallösung $x^*$ von [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]]

Es gilt:
$$\hat{z}\leq z^*$$
denn mit der [[Relaxierung]] kann ein besserer ZFW durch eine für MIP unzulässige Lösung gefunden werden.
Wenn aber $\hat{z}$ für [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] zulässig ist, dann ist es bereits die Optimallösung.

_Das Problem lässt sich in Teilprobleme zerlegen:_

- Sei $x$ gemischt-ganzzahlig
- Sei $s:=\hat{x}_j\notin\mathbb{Z}$ mit $j\in\set{1,...,p}$

Dann ist

- $x$ zulässig für [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] mit $x_j\leq\lfloor s \rfloor$ oder
- $x$ zulässig für [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] mit $x_j\geq\lceil s \rceil$

Seien

- $S$ zulässige Menge für [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]]
- $P$ zulässige Menge für [[LP-Relaxierung]]

_Zwei Annahmen müssen getroffen werden:_

1. [[LP-Relaxierung]] besitzt keine zulässige Lösung oder eine Optimallösung, ist also nicht unbeschränkt.
2. Alle Koeffizienten in $A$ und $b$ sind rational (siehe Übung 7)

## Vorgehen

Löse die [[LP-Relaxierung]], dabei kann es zu folgenden Fällen kommen:

### 1. LP Relaxierung liefert eine ganzzahlige Lösung

Wenn die [[LP-Relaxierung]] eine ganzzahlige Lösung ergibt, so ist [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] gelöst.

### 2. LP Relaxierung liefert eine fraktionale Lösung

Wenn die [[LP-Relaxierung]] keine ganzzahlige Lösung ergibt, so ist die Lösung ein Wert $s$, der nicht ganzzahlig ist.
Partitioniere $S$ mit
$$S_{1}:=S \cap\left\{x: x_{j} \leq\lfloor s\rfloor\right\}, \quad S_{2}:=S \cap\left\{x: x_{j} \geq\lceil s\rceil\right\}$$
Daraus entstehen zwei [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIPs]].

Stelle für die beiden [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIPs]] die entsprechenden LP-Relaxierungen auf mit
$$P_{1}:=P \cap\left\{x: x_{j} \leq\lfloor s\rfloor\right\}, \quad P_{2}:=P \cap\left\{x: x_{j} \geq\lceil s\rceil\right\}$$
Beim lösen der LP-Relaxierungen können folgende Fälle auftreten:

1. [[Prune by Infeasibility]]
2. [[Prune by Integrality]]
3. [[Prune by Bound]]
4. Wenn das Problem einen kleineren ZFW als die beste obere Schranke ([[Prune by Integrality]]) hat, dann kann $S_i$ noch eine optimale Lösung enthalten. Es wird also erneut partitioniert mit $s_{i}:=\hat{x}_{j}^{i}$ und den Mengen $S_{i1}$ und $S_{i2}$. Der Vorgang wird wiederholt.

## Terminiertheit

Der [[Algorithmus]] stoppt, wenn alle Teilprobleme abgearbeitet sind. Das passiert in endlich vielen Schritten, wenn die ganzzahligen Variablen beschränkt sind.
Die Anzahl an Teilproblemen kann aber exponentiell in der Anzahl der ganzzahligen Variablen wachsen.

## Implementierung

Für eine effiziente Implementierung muss noch eine passende Node Selection Rule in Schritt 3 und Branching Rule in Schritt 13 des Algorithmus festgelegt werden.

## Algorithmus

![[Bildschirmfoto 2022-06-23 um 20.20.33.png]]

## Beispiel

$$\min \left\{-5.5 x_{1}-2.1 x_{2}:-x_{1}+x_{2} \leq 2,8 x_{1}+2 x_{2} \leq 17, x_{1}, x_{2} \geq 0, x_{1}, x_{2} \in \mathbb{Z}\right\}$$

Oft wird ein [[Graph]] als Darstellung des Verfahrens verwendet:

![[Bildschirmfoto 2022-06-23 um 20.21.02.png]]
