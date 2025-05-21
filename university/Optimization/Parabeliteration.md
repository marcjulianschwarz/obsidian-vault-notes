---
uni-module: "LNS"
---

# Parabeliteration

Die Abbildung
$$\psi_{\alpha}: \mathbb{R} \rightarrow \mathbb{R}, x \mapsto \alpha x(1-x)$$
mit $\alpha > 0$ und einem Startwert $k^{(0)}\in\mathbb{R}$ erhält man die Iteration
$$k^{(\nu+1)}=\psi_{\alpha}\left(k^{(\nu)}\right), \quad \nu=0,1,2, \ldots$$
woraus die Iterationsfolge folgt.

Lässt man diese Folge gegen Unendlich laufen stellt sich ein Grenzwert $k^*$ ein, der von $\alpha$ abhängig ist.

Sie ist ein Beispiel für eine Iterations Folge bei der das Konvergenzverhalten stark variiert bei Änderung eines Parameters.
Es macht also Sinn einen Weg zu finden zu erkennen wann eine Iterationsfolge konvergiert.

## Konvergenzverhalten

Das **Konvergenzverhalten** variiert je nachdem wie $\alpha$ gewählt wird stark. Wir setzen den Startpunkt $k^{(0)} \in\left(0, \frac{\alpha-1}{\alpha}\right]$

- Für $\alpha\in(1,2]$ liegt der Grenzwert zwischen 0 und 1 bei $k^{*}=\frac{\alpha-1}{\alpha}$ während die Folge monoton wächst
- Für $\alpha\in(2,3)$ ist der Grenzwert der gleiche allerdings fällt die Folge monoton und es liegt eine alternierende Konvergenz vor
- Für $\alpha>3$ ergeben sich zwei Häufungspunkte zwischen denen die Funktion hin und her springt
- Jenseits von $\alpha>3.569$ ist die Funktion pures Chaos

## Beispiele

![[Bildschirmfoto 2022-07-10 um 11.27.08.png]]
