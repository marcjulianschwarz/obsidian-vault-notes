---
uni-module: "LNS"

alias: "Schnittebenenverfahren"
---

# Separierungsproblem

Gegeben sei ein [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] und $x^*\in\mathbb{R}^n$ mit $X$ gemischt-ganzzahlige zulässige Menge von MIP.

Entscheide ob $x^*\in\operatorname{conv}(X)$.
Falls nicht finde eine [[Zulässige Ungleichung]] welche von $x^*$ verletzt wird.

## Lösungsansatz

[[LP-Relaxierung]] von [[Gemischt-ganzzahliges lineares Optimierungsproblem|MIP]] mit Optimallösung $x^*$:

1. Fall $x^*$ ist zulässig für MIP, dann ist MIP gelöst
2. Es muss eine [[Zulässige Ungleichung]] (Schnittebene oder auch cutting plane) geben, die $x^*$ von $\operatorname{conv}(X)$ trennt. Die Ungleichung wird zur [[LP-Relaxierung]] hinzugefügt um die [[Formulierung]] zu verbessern.
3. Iterieren

## Beispiel eines Schnittebenenverfahrens

![[Bildschirmfoto 2022-07-08 um 17.06.37.png]]
