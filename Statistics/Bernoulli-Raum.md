# Bernoulli-Raum

Der Bernoulli-Raum besteht aus einem [[Wahrscheinlichkeitsraum]], der durch das Tripel $(\Omega, \mathcal{A}, P)$ aufgespannt wird. Dabei ist $\Omega=\{0,1\}$ und $\mathcal{A}$ ist die [[Potenzmenge]] von $\Omega$.
Die [[Wahrscheinlichkeitsmaß|Verteilung]] P ist definiert durch:
- $P(\emptyset) = 0$
- $P\{1\}) = p$
- $P(\{0\}) = 1-p$
- $P(\{0,1\})=1$

mit dem Parameter $p \in [0,1]$.

Diese [[Wahrscheinlichkeitsmaß|Verteilung]] nennt sich auch [[Bernoulli-Verteilung]] ($Ber_p$)

## Was kann man damit machen?
Mit dem Bernoulliraum lassen sich einfache Zufallsexperimente modellieren. Um das zu tun weißt man den Werten 0 und 1 verschiedene [[Ereignis | Ereignisse]] zu (z.B. Kopf und Zahl beim Münzwurf).
Bei einem solchen speziellen Experiment lässt sich aus $P(\{1\})$ direkt die ganze [[Wahrscheinlichkeitsmaß|Verteilung]] ableiten (das ist aber allgemein nicht möglich).
Um  diese [[Wahrscheinlichkeitsmaß|Verteilung]] der 1 herauszufinden braucht man die [[Relative Häufigkeit]].

Wenn man aber a priori plausible Annahmen macht (z.B. dass die Münze oder der Würfel fair ist), dann kann man $p$ auch direkt bestimmen als $P(\{k\})=\frac{1}{|\Omega|}$.
Das geht so, weil die [[Elementarereignis | Elementarereignisse]] die gleiche Wahrscheinlichkeit haben. 
Da $\Omega$ endlich ist und durch [[Sigma-Additivität]] lässt sich für $A\subset \Omega$ die [[Wahrscheinlichkeitsmaß|Verteilung]] als $P(A)=\sum_{w\in A}{P(\{w\})}=\frac{|A|}{|\Omega|}$ berechnen.

→ Das Modell ist nun vollständig