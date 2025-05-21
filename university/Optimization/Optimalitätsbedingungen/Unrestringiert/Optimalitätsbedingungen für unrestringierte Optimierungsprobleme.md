---
uni-module: "LNS"
---

# Optimalitätsbedingungen für unrestringierte Optimierungsprobleme

Notwendige Bedingungen → Optimalpunkte auffinden
Hinreichende Bedingungen → Punkt auf Optimalität überprüfen

Ist $\widetilde{x}$ [[lokales Minimum]] ([[Stetigkeit|stetig]] in $\widetilde{x}$) von $(P_u)$ dann gilt:
$$\nabla f(\widetilde{x})^Td\geq0$$
$$\forall d\in\mathbb{R}^n$$
Da diese Aussage für alle Richtungen gilt, gilt sie auch für $-d$ woraus durch Umformung die [[Notwendige Optimalitätsbedingung erster Ordnung unrestringierter Probleme]] folgt.

Diese Bedingung führt zu einer direkten Lösung der [[Linear Regression|Linearen Regression]] mit
$$\tilde{x}_{1}=\frac{\sum_{i=1}^{m} \xi_{i} \eta_{i}-\frac{1}{m} \sum_{i=1}^{m} \xi_{i} \sum_{i=1}^{m} \eta_{i}}{\sum_{i=1}^{m} \xi_{i}^{2}-\frac{1}{m}\left(\sum_{i=1}^{m} \xi_{i}\right)^{2}}, \quad \tilde{x}_{2}=\frac{1}{m}\left(\sum_{i=1}^{m} \eta_{i}-\tilde{x}_{1} \sum_{i=1}^{m} \xi_{i}\right) .$$

Ein [[Sattelpunkt]] ist ein spezieller [[Stationärer Punkt]], bei dem $f$ weder das [[lokales Minimum]] noch das [[lokales Maximum]] ist.

Um zwischen Minima, Maxima und Sattelpunkten zu unterscheiden muss das Krümmungsverhalten untersucht werden. Dies führt auf die [[Notwendige Optimalitätsbedingung zweiter Ordnung]].

Allerdings reichen selbst beide Bedingungen nicht aus um sicher zu gehen, dass ein Minimum vorliegt. Durch eine Verschärfung der Bedingung zweiter Ordnung ist es allerdings möglich auf die [[Hinreichende Optimalitätsbedingung zweiter Ordnung]] zu kommen.

### Optimalitätsbedingungen

- [[Notwendige Optimalitätsbedingung erster Ordnung unrestringierter Probleme]]
- [[Notwendige Optimalitätsbedingung zweiter Ordnung]]
- [[Hinreichende Optimalitätsbedingung zweiter Ordnung]]

Aus [[Konvexe Funktion|Konvexität]] folgt direkt, dass $\widetilde{x}$ eine globale Lösung ist, wenn $\nabla f(\widetilde{x})=0$ ist.
