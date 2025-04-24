---
uni-module: "StochMod"
---

# Der Poisson-Prozess

Die Beschreibung der Anzahl der [[Ereignis|Ereignisse]], die in einem gegebenen Intervall eintreten.

$n$ [[stochastisch unabhängig]]e [[Zufallsvariable|Zufallsvariablen]] (in die [[Borel Sigma Algebra|Borel Mengen]]) mit [[Gleichverteilung]] auf dem Intervall $[0, t_n]$ . Die [[Zufallsvariable]] wird als der zufällige Eintritt von einem [[Ereignis]] $i$ interpretiert.

Für $[\alpha,\beta]\subset [0,t_n]$ gilt:

$$
\begin{aligned}
N_{[\alpha, \beta]}^{(n)} &:=\left|\left\{i \in\{1, \ldots, n\}: X_{i} \in[\alpha, \beta]\right\}\right| \\
&=\sum_{i=1}^{n} \mathbb{1}_{[\alpha, \beta]}\left(X_{i}\right) .
\end{aligned}
$$

Dann ist $N$ eine [[Zufallsvariable]]. Die [[Wahrscheinlichkeitsmaß|Verteilung]] ist eine [[Binomialverteilung]] mit $p=\frac{\beta-\alpha}{t_n}$.

Die [[Wahrscheinlichkeitsmaß|Verteilung]] ist also nur von der Länge des Intervalls (also $\alpha-\beta$) abhängig und nicht von der Lage.

Hier fehlt noch die Sprungstellen in der zufälligen Funktion von $N$.

Allerdings weiß man in den meisten Situation gar nicht wie viele [[Ereignis|Ereignisse]] ($n$) eintreten werden. Wir sind also eher an einem unbeschränkten Zeitraum wie $[0,\infty)$ interessiert.
Also brauchen wir unendlich viele [[Zufallsvariable|Zufallsvariablen]]. Allerdings muss man aufpassen, dass die Länge des Intervalls ($t_n$) und die Anzahl der [[Zufallsvariable|Zufallsvariablen]] ($n$) geeignet gekoppelt werden. → [[Kopplung]]

Es stellt sich heraus, dass $N$ nun [[Poisson Verteilung|poisson verteilt]] ist.

Für zwei "fast disjunkte" Intervalle gilt im [[Asymptotisches Regime großer Gesamtheiten]], dass die Anzahl an Ereignissen in diesen Intervallen [[stochastisch unabhängig]] sind. Diese Beobachtung gilt auch für endlich viele Intervalle.

$(N_t)_{t\geq0}$ ist also ein Poisson-Prozess mit Intensität $\lambda>0$ , wenn folgende Eigenschaften gelten:

1. $N_0=0$
2. $N_{t1}-N_{t0},N_{t2}-N_{t1},...,N_{t_n}-N_{t_{n-1}}$ sind [[stochastisch unabhängig]]
3. Es gibt ein $\lambda>0$ mit $N_t-N_s$~$\operatorname{Poi}_{\lambda(t-s)}$
