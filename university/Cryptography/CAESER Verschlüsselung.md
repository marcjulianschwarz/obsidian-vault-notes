---
uni-module: "KRY"

alias: "CAESER"
---

# CAESER Verschlüsselung

> [!TIP] [[Alphabet]] > $A,\dots, Z$ identifiziert mit den Zahlen $0,\dots,25$

> [!TIP] [[Schlüssel]]
> Ganze Zahl $k$

Verschlüsselungsfunktion
$$f_{k}(x)=(x+k)\quad \text{mod}\quad 26$$

Die Entschlüsselungsfunktion sieht entsprechend so aus
$$f^{-1}_{k}(x)=(x-k)\quad\text{mod}\quad 26$$

Man bemerkt schnell, dass es für diese Verschlüsselung nur maximal 26 verschiedene Schlüssel geben kann. Es reicht also alle diese Schlüssel auszuprobieren und den entschlüsselten Text auf Sinnhaftigkeit zu überprüfen um den richtigen Schlüssel zu finden.

Es wäre also sinnvoll CAESAR zu verallgemeinern, indem man für $f_{k}$ beliebige Permutation ([[Bijection|Bijektion]]) zulässt. Das führt auf die [[MASC-Verschlüsselung]].
