---
uni-module: LKO

alias: ["konvex", "Konvexität"]
---

# Konvexe Funktion

Eine Funktion ist konvex auf $K$ ([[Konvexe Menge]]), wenn gilt:
$$f(tx+(1-t)y) \leq tf(x)+(1-t)f(y)$$
beziehungsweise

$$f(y)+\nabla f(y)^T(x-y)\leq f(x)$$

beziehungsweise strikt konvex, wenn [[Hessematrix]]:

$$\nabla^2 f(x)$$
[[Definitheit|positiv definit]], also wenn der [[Definitheit|Hauptminorenkriterium]] erfüllt ist, also wenn alle Hauptminoren größer als 0 sind.

Einmal differenzierbare Funktion mit einer Veränderlichen ist konvex, wenn jede Tangente unterhalb des Graphen liegt oder mit diesem zusammenfällt.

![[IMG - konvexe Funktion.jpeg]]

strikt konvex, wenn $<$ und $x\neq y$

![[Bildschirmfoto 2022-05-13 um 12.11.21.png]]
