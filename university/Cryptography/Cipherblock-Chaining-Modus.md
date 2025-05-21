---
uni-module: "KRY"

alias: "CBC-Modus"
---

# Cipherblock-Chaining-Modus

- [[Alphabet]] sind natürliche Zahlen $0\dots N-1$.
- Klartext wird in Blöcke $a_{i}$ der Länge $k$ aufgeteilt.
- Initialisierungsvektor $b_{0}$ der Länge $k$ wird gewählt

Damit ergibt sich die folgende _verschobene_ Verschlüsselungsfunktion:
$$b_i=E_K\left(b_{i-1}+a_i\right)$$
wobei das $+$ in diesem Fall eine Addition modulo $N$ darstellt.

Die Entschlüsselung erfolgt demnach mit:

$$
a_i=D_K\left(b_i\right)-b_{i-1}\quad (\bmod N)
$$
