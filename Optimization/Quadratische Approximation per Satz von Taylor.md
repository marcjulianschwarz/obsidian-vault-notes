---
uni-module: "LNS"
---

# Quadratische Approximation per Satz von Taylor

Gegeben sei eine [[Stetigkeit|stetige]] Funktion $f$, die zweimal differenzierbar ist auf einer nichtleeren, offenen und [[Konvexe Menge|konvexen Menge]] in die reelen Zahlen, dann gilt:

$$f(x)=f\left(x_{0}\right)+\nabla f\left(x_{0}\right)^{\top}\left(x-x_{0}\right)+\frac{1}{2}\left(x-x_{0}\right)^{\top} \nabla^{2} f\left(x_{0}\right)\left(x-x_{0}\right)+o\left(\left\|x-x_{0}\right\|^{2}\right)$$
$$f(x)=f\left(x_{0}\right)+\nabla f\left(x_{0}\right)^{\top}\left(x-x_{0}\right)+\frac{1}{2}\left(x-x_{0}\right)^{\top} \nabla^{2} f(\xi)\left(x-x_{0}\right)$$
$$f\left(x_{0}+p\right)=f\left(x_{0}\right)+\nabla f\left(x_{0}\right)^{\top} p+\frac{1}{2} p^{\top} \nabla^{2} f\left(x_{0}+\theta p\right) p$$
$$f\left(x_{0}+p\right)=f\left(x_{0}\right)+\nabla f\left(x_{0}\right)^{\top} p+\frac{1}{2} p^{\top} \nabla^{2} f\left(x_{0}\right) p+o\left(\|p\|^{2}\right)$$
→ siehe Skript wegen Herleitung der anderen Formen.
