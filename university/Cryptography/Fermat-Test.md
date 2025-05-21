---
uni-module: "KRY"
---

# Fermat-Test

Der Fermat-Test zur Basis $a$ basiert auf dem [[Kleiner Satz von Fermat|Kleinen Satz von Fermat]]. Wir testen also für eine Zahl ob
$$a^{p-1}\equiv1\bmod p$$
gilt (zum Beispiel mit der [[Square-And-Multiply-Methode zum Potenzieren|Square-And-Multiply-Methode]]). Ist dies der Fall, dann kann die Zahl $p$ eine [[Primzahl]] sein.

Leider ist es aber möglich, dass auch eine zusammengesetzte Zahl diese Kongruenzgleichung erfüllt. Diese Zahlen nennt man auch [[Pseudoprimzahl]].

Es fällt allerdings auf, dass die Anzahl an Pseudoprimzahlen im Vergleich zu echten Primzahlen sehr gering ist.

Wir schätzen die Anzahl der Primzahlen kleiner gleich $x$ mit
$$\pi(x) \sim \frac{x}{\log x}.$$

Damit gilt dann nach Erdös:
$$\lim _{x \rightarrow \infty} \frac{\pi_{\text {Fermat }, a}(x)}{\pi(x)}=0.$$

Eine Zahl, die einen oder mehrere Tests (zu unterschiedlichen Basen) besteht, nennt man auch eine **wahrscheinliche Primzahl**.
Normalerweise testet man vorher mit den bereits genannten Methoden auf kleine Teiler und nutzt dann einen Primzahltest wie den Fermattest auf den übrig gebliebenen Zahlen.

Ein Problem dieses Tests sind sogenannte [[Carmichael-Zahl|Carmichael-Zahlen]], die für alle Basen den Test bestehen obwohl sie [[Pseudoprimzahl|Pseudoprimzahlen]] sind.
