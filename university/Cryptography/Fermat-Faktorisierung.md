---
uni-module: "KRY"
---

# Fermat-Faktorisierung

Wir wollen $N$, eine ungerade natürliche Zahl faktorisieren. Bei der Fermatschen Faktorisierungsmethode versucht man nun die Zahl $N$ als Differenz von Quadratzahlen zu schreiben:
$$N=u^2-w^2,$$
denn dann erhält man die Zerlegung
$$N=(u-w)(u+w).$$

Wir schreiben
$$u^2-N=w^2$$
und erkennen, dass $u^2\geq N$ und damit auch $u\geq \lceil\sqrt{N}\rceil.$

Wir testen also für
$$u=\lceil\sqrt{N}\rceil,\lceil\sqrt{N}\rceil+1,\lceil\sqrt{N}\rceil+2,\lceil\sqrt{N}\rceil+3,\dots$$
ob $u^2-N$ eine Quadratzahl ist.
