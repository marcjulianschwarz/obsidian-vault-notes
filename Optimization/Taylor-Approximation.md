---
uni-module: LNS
aliases:
  - Taylor Expansion
---
# Taylor-Approximation

- [[Lineare Approximation per Satz von Taylor]]
- [[Quadratische Approximation per Satz von Taylor]]

## Anwendung

Oft sind nichtlineare Optimierungsprobleme schwer zu lösen oder es ist schwer zulässige Punkte zu finden.
In solchen Fällen kann man die schwierigen Gleichungen durch ihre Taylor Approximationen ersetzen. Wenn man zum Beispiel eine Taylor-Approximation mit $n=1$ also [[Lineare Approximation per Satz von Taylor]] macht ergibt sich ein lineare Problem, welches man zum Beispiel durch das [[Jacobi-Verfahren]] lösen kann.
Mit der Lösung kann man dann wieder eine Linearisierung durchführen und kommt somit der echten Lösung iterativ näher.
Die [[Konvergenz]] dieses Verfahrens ist sehr gut. #confirm
