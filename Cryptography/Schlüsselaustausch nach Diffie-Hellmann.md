---
uni-module: "KRY"
---

# Schlüsselaustausch nach Diffie-Hellmann

Das erste Public-Key-Verfahren.

- [[Primzahl]] $p$
- Zahl $g$ mit $2\leq g\leq p-2$

Person A wählt eine Zahl $e_A$ mit $0\leq e_A\leq p-2$ und berechnet seinen [[Address|Public Key]] mit
$$f_A=g^{e_A}\bmod p.$$

Peson B geht genauso vor und erhält damit den Public Key $f_B$.

Person A und B haben einen gemeinsamen Schlüssel
$$k_{AB}=g^{e_Ae_B}\bmod p$$
, den sich beide Personen selbst mit ihrem [[Private Key]] und dem [[Address|Public Key]] des anderen berechnen können

$$
\begin{aligned}
& k_{A B}=f_B^{e_A} \bmod p \\
& k_{A B}=f_A^{e_B} \bmod p
\end{aligned}.
$$
