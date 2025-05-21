---
uni-module: "LNS"
---

# Rosenbrock-Funktion

Häufig verwendete Testfunktion in der Optimierungsliteratur.

$$g(x_1,x_2) = 100 (x_2 - x_1^2)^2 + (1 - x_1)^2$$

![[rosenbrock.png]]

Das [[Gradientenverfahren]] hat hier Probleme, dass es ständig von Seite zu Seite springt, die [[Armijo-Schrittweitenregel]] sucht womöglich zu große Schritte aus.
