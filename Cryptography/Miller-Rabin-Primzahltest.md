---
uni-module: "KRY"
---

# Miller-Rabin-Primzahltest

Eine Verfeinerung des [[Fermat-Test]].

Im [[Fermat-Test]] haben wir die Eigenschaften einer [[Primzahl]] bzgl des [[Kleiner Satz von Fermat|Kleinen Satz von Fermat]] verwendet um [[Primzahl|Primzahlen]] und [[Pseudoprimzahl|Pseudoprimzahlen]] zu bestimmen.
Leider gibt es [[Carmichael-Zahl|Carmichael-Zahlen]], die den Test immer bestehen, man kann diese also nie als zusemmengesetzte Zahlen ausschließen.

Der Miller-Rabin Test verwendet eine weitere Eigenschaft von Primzahlen.
Für eine [[Primzahl]] $p$ und eine Zahl $a$ mit
$$a^2\equiv 1\bmod p$$
und
$$a\not\equiv 1\bmod p$$
gilt
$$a\equiv-1\bmod p.$$

Wir verwenden diese Eigenschaft um folgendes Lemma zu zeigen.

Sei $p$ eine ungerade [[Primzahl]]. Wir zerlegen $p-1$ in
$$p-1=2^lq$$, wobei $q$ ungerade ist,
$$ggT(a,p)=1$$
und
$$b=a^q\bmod p.$$

Dann gilt für $b$, entweder
$$b\equiv 1\bmod p$$
oder es gibt ein $i\leq l-1$ mit
$$b^{2^i}\equiv -1\bmod p.$$

Wir sehen, dass zusammengesetzte Zahlen, [[Pseudoprimzahl|Pseudoprimzahlen]] und sogar [[Carmichael-Zahl|Carmichael-Zahlen]] dieses Lemma nicht erfüllen.

Wir verwenden diese Überlegung als Miller-Rabin Test zur Basis $a$.

code ...

Leider gibt es auch hier analog zu den [[Pseudoprimzahl|Fermat-Pseudoprimzahlen]] sogenannte [[Miller-Rabin-Pseudoprimzahl|Miller-Rabin-Pseudoprimzahlen]], die den Test bestehen, obwohl sie keine [[Primzahl|Primzahlen]] sind.

Der Miller-Rabin Test wird immer zur Basis $a=n-1$ bestanden. Es macht also Sinn nur für $a\in\{2,\dots,n-2\}$ zu testen.

Außerdem gilt
$$\#E(n)=\#\{a \in\{2,3, \ldots, n-1\}: n \text { besteht zur Basis } a\}<\frac{1}{4} \varphi(n)<\frac{1}{4} n$$
Die Wahrscheinlichkeit, dass eine ungerade natrüliche Zahl eine Primzahl ist, nach $r$ bestandenen Miller-Rabin-Tests ist
$$\geq1-\left(\frac{1}{4}\right)^r.$$
Wir sprechen auch hier immer noch nur von wahrscheinlichen Primzahlen.
