---
uni-module: "LNS"
---

# Kontinuierliche Reformulierung von ganzzahligen Variablen

Durch ganzzahlige Variablen in [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLPs]] kann man keine [[Nichtlineares Optimierungsproblem|NLP]] Algorithmen anwenden. Daher macht es Sinn diese kontinuierlich zu reformulieren.

Die oberen und unteren Schranken $u$ und $l$ des [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLP]] können wir als ganzzahlig annehmen.

Wir können also $z_j\in\{0, ..., u_j\}$ als:

$$z_{j}=2^{0} z_{j}^{0}+2^{1} z_{j}^{1}+2^{2} z_{j}^{2}+2^{3} z_{j}^{3}+\ldots+2^{k_{j}} z_{j}^{k_{j}}$$
binär darstellen mit $z_j^i \in\{0,1\}$ für $i=0,1,...\lfloor \operatorname{log}_2u_j\rfloor$ .
Eine weitere Darstellung wäre durch

$$z_{j}=z_{j}^{1}+z_{j}^{2}+z_{j}^{3}+\ldots+z_{j}^{u_{j}}$$
möglich, hier mit linear vielen Binärvariablen.

Nun müssen wir also nur noch eine Möglichkeit finden Binärvariablen kontinuierlich zu reformulieren, dann können wir beliebige ganzzahlige Variablen durch kontinuierliche Variablen darstellen.

Wir verwenden eine [[Komplementaritätsbedingung]] mit $n=2$ und $\psi(x,y)=y$ und $\phi(x,y)=y$ zusammen mit der Bedingung $x+y=1$ und modellieren somit den Bereich $\{(0,1)^T,(1,0)^T\}\subseteq \mathbb{R}^2$, welcher nur aus den beiden Punkten besteht.

Nun könen wir jede binäre Variable durch $x,y$ mit den oben beschriebenen Bedingungen ersetzen und identifizieren $(0,1)$ als $0$ und $(1,0)$ als $1$.
Somit ist es jetzt möglich ein [[Gemischt-ganzzahliges nichtlineares Optimierungsproblem|MINLP]] in ein [[Nichtlineares Optimierungsproblem|NLP]] umzuformen. Dabei entsteht allerdings der Nachteil, dass keiner der zulässigen Punkte die [[Linear Independence Constraint Qualification|LICQ]] erfüllt und man somit nicht mehr überprüfen kann ob unter den KKT-Punkten das Minimum vorhanden ist.

- [[NCP-Funktion]]

### Vor- und Nachteile der Reformulierungen

| Reformulierung                     | Für                                                                      | Wieder                                                                        |
| ---------------------------------- | ------------------------------------------------------------------------ | ----------------------------------------------------------------------------- |
| [[Komplementaritätsbedingung]]     | Glattheit                                                                | globale Verletzung der [[Linear Independence Constraint Qualification\|LICQ]] |
| [[NCP-Funktion]]                   | kein Einfluss auf [[Linear Independence Constraint Qualification\|LICQ]] | schlechte Glattheit und $\eta$ schwierig auszuwerten                          |
| [[Parabelfunktion-Reformulierung]] | Glattheit                                                                | lokale Verletzung der [[Linear Independence Constraint Qualification\|LICQ]]  |
