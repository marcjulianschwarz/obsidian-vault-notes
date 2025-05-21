---
uni-module: "StochMod"
---

# Multinomialverteilung

> **"Anzahl der Treffer bei n Versuchen"**

- [[Urnenmodell]]
- $N$ durchnummerierte Kugeln
- Jede Kugel ist mit einer aus $r$ Farben markiert
  - Dafür teilt man die Kugeln in $r$ Gruppen ($M_r$ ist die Anzahl der Kugeln der Farbe $r$) auf und gibt ihnen jeweils die Farbe
- $n$ Kugeln ziehen _mit Zurücklegen_ und _mit Beachtung der Reihenfolge_
- Wahrscheinlichkeit, dass unter den gezogenen Kugeln genau $k_i$ Kugeln der Farbe $i$ haben

## [[Wahrscheinlichkeitsraum|W-Raum]] aufstellen

- [[Grundraum]] → $\Omega=\set{1,...,N}^n$ → Tupel
- $|\Omega|=N^n$
- [[Sigma Algebra]] → $\mathcal{A}=\mathbb{P}(\Omega)$
- [[Gleichverteilung]] mit $\frac{1}{N^n}$

---

Um die Wahrscheinlichkeit eines Ereignises zu berechnen braucht man zuerst die Kardinalität von dem [[Ereignis]].
In diesem Fall haben wir mehrere Parameter:

- $k_i$ → Anzahl der gezogenen Kugeln mit der Farbe $i$
- $M_r$ → Anzahl der Kugeln mit der Farbe $r$
- $n$ → Anzahl der gezogenen Kugeln

_Für die 1. Farbe gilt:_
Es gibt $\binom{n}{k_1}$ mögliche Positionen dieser Farbe in den $n$ gezogenen Kugeln (wegen mit Beachtung der Reihenfolge).
Zusätzlich können an den "ausgewählten" Positionen $M_1^{k_	1}$ verschiedene Kugeln sein (wegen mit Zurücklegen).

_Für die 2. Farbe gilt:_
Es gibt dementsprechend nur noch $\binom{n-k_1}{k_2}$ mögliche Positionen, da bereits $k_1$ Plätze belegt sind.

_Für die letzte Farbe gilt_:
Es ist nur noch eine mögliche Position übrig.

---

Für die Kardinalität eines Ereignises $A_{k_1,...,k_r}$ gilt also:

$$\binom{n}{k_1}M_1^{k_1}\binom{n-k_1}{k_2}M_2^{k_2}...\binom{n-k_1-...-k_{r-1}}{k_r}M_r^{k_r}$$

Diese Formel sieht dann zusammengefasst so aus:
$$\frac{n!}{k_1!...k_r!}M_1^{k_1}...M_r^{k_r}$$
→ Der Bruch ist der sogenannte [[Multinomialkoeffizient]]

---

Damit folgt am Ende die [[Wahrscheinlichkeitsmaß|Verteilung]]:
$$P(A_{k_1,...,k_r})=\frac{1}{N^n}\binom{n}{k_1,...,k_r}M_1^{k_1}...M_r^{k_r}$$

Umgeschrieben kommt man auf eine Form, in der man nicht mehr die Anzahl der einzelnen gefärbten Kugeln angibt sondern den Anteil einer Farbe an allen Kugeln durch den Parameter $p_r \in [0,1]$:

$$\binom{n}{k_1,...,k_r}(\frac{M_1}{N})^{k_1}...(\frac{M_r}{N})^{k_r}$$
