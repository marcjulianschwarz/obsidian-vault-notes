---
uni-module: "StochMod"

alias: "De Morgansche Gesetze"
---

# De-morgansche Regeln

## Aussagenlogik

$$
\begin{aligned}
& \neg(\phi \wedge \psi) \equiv(\neg \phi \vee \neg \psi) \\
& \neg(\phi \vee \psi) \equiv(\neg \phi \wedge \neg \psi)
\end{aligned}
$$

## Mengenlehre

$$
\begin{aligned}
&\overline{A \cap B}=\bar{A} \cup \bar{B} \\
&\overline{A \cup B}=\bar{A} \cap \bar{B} .
\end{aligned}
$$

Gelten auch für endlich viele Verknüpfungen.

$$\overline{\bigcap_{i \in I} A_{i}}=\bigcup_{i \in I} \overline{A_{i}} \text { und } \overline{\bigcup_{i \in I} A_{i}}=\bigcap_{i \in I} \overline{A_{i}}$$

Können z.B. nützlich sein zum beweisen für [[Sigma Algebra]] Eigenschaften.

In Code sehen sie so aus:

```
!(x||y) === !x & !y
```
