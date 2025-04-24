---
uni-module: MFDS
---

# Fixpunktsatz von Banach

## Voraussezungen:

- Es sei $(X,d_X)$ ein vollständiger [[Banachraum]]
- → jede [[Cauchy-Folge]] mit Elementen des Raums [[Konvergenz|konvergiert]] im Raum
- Es sei $A$ Teilmenge von $X$ abgeschlossen bezüglich $d_X$
- $A$ soll nicht leer sein
- eine Selbstabbildung $\phi$ von $A$ nach $A$ (kontrahierend)
- [[Lipschitz-stetig]] mit einer Konstante kleiner 1 und größer gleich 0 ([[Kontraktion]])

## Es gilt

- $\phi$ besitzt genau einen Fixpunkt
- also gilt $\begin{equation} \phi(\bar{x})=\bar{x}\end{equation}$

Das [[Iterationsverfahren]]:
$$x^{(0)}$$
$$x^{(k+1)}=\phi(x^{(k)})$$
[[Konvergenz|konvergiert]] für jeden Startpunkt gegen den Fixpunkt.

## Beweisskizze

Es müssen folgende Aussagen nacheinander gezeigt werden:

1. Die Iterationsfolge ist eine [[Cauchy-Folge]]
2. Der Grenzwert dieser Folge ist ein [[Fixpunkt]]
3. Es existiert nur genau eine [[Fixpunkt]]

Zuerst zeigen wir, dass die Iterationsfolge eine [[Cauchy-Folge]] ist, denn mit der Voraussetzung eines vollständigen [[Banachraum|Banachraums]] wissen wir, dass die Folge dann im Raum [[Konvergenz|konvergiert]].
Danach muss noch gezeigt werden, dass der Grenzwert dieser Folge ein Fixpunkt ist.
Zuletzt beweisen wir, dass nur genau ein Fixpunkt existiert.

## Vergleich

Auch das [[Newton Verfahren]] kann verwendet werden um Fixpunkte zu berechnen. Es [[Konvergenz|konvergiert]] noch schneller.
