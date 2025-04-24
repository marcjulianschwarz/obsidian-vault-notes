---
uni-module: "LNS"
---

# Das Gesamtschrittverfahren zur Lösung linearer Gleichungssysteme

Um ein [[Lineares Gleichungssystem]] mit dem [[Jacobi-Verfahren]] lösen zu können muss es zuerst in die [[Fixpunktform]] gebracht werden.

Lösen von linearen Gleichungssystemen der Form $Ax=b$.

Wir verwenden die [[Maximumsnorm]] um die Lipschitz-Konstante der Fixpunktform abzuschätzen.

[[Induzierte Matrixnorm]]

Das Konvergenzverhalten eines [[Iterationsverfahren]] hängt unter anderem von den Eigenwerten der Iterationsmatrix ab.
Das [[Spektrum]] und der dazugehörige [[Spektralradius]] spielen dabei also eine zentrale Rolle.

Das [[Iterationsverfahren]] für ein [[Lineares Gleichungssystem|LGS]] in [[Fixpunktform]] konvergiert genau dann für jeden beliebigen Startvektor gegen die Lösung, wenn der [[Spektralradius]] der Matrix $T$ kleiner als 1 ist.
Um den [[Spektralradius]] abschätzen zu können kann man eine [[Induzierte Matrixnorm]] verwenden, denn für jede dieser Normen gilt, dass $\rho(A)\leq ||A||$ ist.
Diese Abschätzung kann zum Beispiel mit der von der [[Maximumsnorm]] induzierten Matrixnorm, der [[Zeilensummennorm]] einfach gemacht werden.

Aus dem [[Fixpunktsatz von Banach]] folgt dann, wenn die [[Zeilensummennorm]] von $T$ kleiner als 1 ist, dass das [[Lineares Gleichungssystem|LGS]] in [[Fixpunktform]] für jedes $u$ eine eindeutige Lösung hat und das Iterationsverfahren für jeden Startvektor gegen diese Lösung kovergiert.

Durch [[Umwandlung LGS in Fixpunktform]] lässt sich das [[Jacobi-Verfahren]] nun durchführen.
Das [[Zeilensummenkriterium]] bietet eine einfache Möglichkeit das Konvergenzverhalten des [[Jacobi-Verfahren]] schon vorher durch die Matrix $A$ zu bestimmen ohne die Umformung in [[Fixpunktform]] vonehmen zu müssen.
