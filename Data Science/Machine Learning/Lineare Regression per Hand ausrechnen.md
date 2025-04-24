---
uni-module: EMD
---

# Lineare Regression per Hand ausrechnen

[[Linear Regression]]

1. Matrix aufstellen
2. Gewichte w berechnen
3. Funktion mit Gewichten und Basis aufstellen

Matrix:

$$
\begin{equation}
\Phi=\left(\begin{array}{cccc}
\phi_{0}\left(x_{1}\right) & \phi_{1}\left(x_{1}\right) & \cdots & \phi_{M-1}\left(x_{1}\right) \\
\phi_{0}\left(x_{2}\right) & \phi_{1}\left(x_{2}\right) & \cdots & \phi_{M-1}\left(x_{2}\right) \\
\vdots & \vdots & \ddots & \vdots \\
\phi_{0}\left(x_{N}\right) & \phi_{1}\left(x_{N}\right) & \cdots & \phi_{M-1}\left(x_{N}\right)
\end{array}\right)
\end{equation}
$$

Berechnung der Gewichte (falls die Spalten der Matrix linear unabhängig sind):

$$
\begin{equation}
\left(\Phi^{T} \Phi\right)^{-1} \Phi^{T} y
\end{equation}
$$

oder das GLS lösen:

$$
\begin{equation}
\Phi^{T} \Phi w=\Phi^{T} y
\end{equation}
$$
