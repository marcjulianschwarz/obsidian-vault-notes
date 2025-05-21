---
uni-module: "KRY"

alias: ["Starke Pseudoprimzahl"]
---

# Miller-Rabin-Pseudoprimzahl

Analog zu [[Pseudoprimzahl|Fermat-Pseudoprimzahl]] für den [[Miller-Rabin-Primzahltest]].

Eine zusammengesetzte ungerade natürliche Zahl (also keine [[Primzahl]]), die den [[Miller-Rabin-Primzahltest]] besteht.

## Beispiel

$n=2047=23\cdot89.$ Es ist
$$n-1=2\cdot 1023$$
mit $l=1$.
Für $a=2$ berechnen wir
$$b=(2^{1023}\bmod n)=1.$$
Somit ist der Test bestanden.
