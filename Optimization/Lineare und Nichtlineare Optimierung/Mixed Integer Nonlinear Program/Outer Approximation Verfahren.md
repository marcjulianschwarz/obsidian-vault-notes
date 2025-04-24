---
uni-module: "LNS"

tags: Algorithmus
---

# Outer Approximation Verfahren

Häufig bessere Performance als das [[Branch-and-Bound Verfahren]].

Die Idee ist statt [[NLP-Relaxierung|NLP-Relaxierungen]] zu lösen MIP-Relaxierungen zu lösen, da wir [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIPs]] verhältnismäßig gut lösen können.

Das Verfahren beruht unter folgenden

## Annahmen

- $P$ ist [[Polytop]]
- Zielfunktion und nichtlineare Nebenbedinungen sind [[Konvexe Funktion|konvex]] und einmal [[Stetigkeit|stetig]] differenzierbar
- Eine [[Constraint Qualification]] ist bei jeder Lösung des NLP Subproblems erfüllt

Die größte Einschränkung ist die [[Konvexe Funktion|Konvexität]], die gefordert wird. Der [[Algorithmus]] funktioniert auch auf nicht konvexen Problemen, dann ist allerdings nicht garantiert, dass er zu einem globalen Optimum führt.

## Algorithmus

In diesem Verfahren werden abwechselnd [[NLP-Relaxierung|NLP-Relaxierungen]] und MIP-Relaxierungen des Ursprungsproblem gelöst.

- Löse [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]]
- Fixiere [[NLP-Relaxierung]] auf ganzzahligen Teil der MIP Lösung
- Löse [[Nichtlineares Optimierungsproblem|NLP]]

→ 2 Fälle:

### NLP hat Lösung

Für alle Lösungen des Ursprungsproblem gelten die folgenden Ungleichungen (siehe [[Lineare Approximation per Satz von Taylor]]) :

$$
\begin{aligned}
&f(\bar{x}, \bar{z})+\nabla f(\bar{x}, \bar{z})^{\top}\left(\begin{array}{c}
x-\bar{x} \\
z-\bar{z}
\end{array}\right) \leq \eta \quad \text { und } \\
&c_{i}(\bar{x}, \bar{z})+\nabla c_{i}(\bar{x}, \bar{z})^{\top}\left(\begin{array}{c}
x-\bar{x} \\
z-\bar{z}
\end{array}\right) \leq 0 \quad \text { für alle } \quad i \in \mathcal{I} .
\end{aligned}
$$

### NLP ist unzulässig

Nach lösen des [[Zulässigkeitsproblem]] gelten diese Ungleichungen:

$$0 \geq c_{i}(\bar{x}, \bar{z})+\nabla c_{i}(\bar{x}, \bar{z})^{\top}\left(\begin{array}{c}x-\bar{x} \\ z-\bar{z}\end{array}\right) \quad \text{für alle} \quad i \in \mathcal{I}^{\text {inf }}$$
$$0 \geq c_{i}(\bar{x}, \bar{z})+\nabla c_{i}(\bar{x}, \bar{z})^{\top}\left(\begin{array}{c}x-\bar{x} \\ z-\bar{z}\end{array}\right) \quad \text{für alle} \quad i \in \mathcal{I} \backslash \mathcal{I}^{\inf }$$

- Nun können die generierten Ungleichungen dem [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] hinzugefügt werden, welches erneut gelöst werden kann um neue Fixierungen zu berechnen.
- Der Algorithmus terminiert wenn das MIP nicht mehr zulässig ist

![[Bildschirmfoto 2022-07-15 um 11.12.24.png]]

## Arbeitsweise für ein Beispiel

![[Bildschirmfoto 2022-07-15 um 11.13.04.png]]
