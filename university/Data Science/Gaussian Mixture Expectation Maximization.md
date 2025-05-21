---
uni-module: EMD
---
# Gaussian Mixture Expectation Maximization

Dieser Algorithmus basiert auf der Vorstellung, dass unsere Daten nicht nur gegeben sind sondern sie eine Art Stichprobe einer unbekannten Wahrscheinlichkeitsverteilung sind. Wenn man also diese Wahrscheinlichkeitsverteilung herausfindet kann man die Daten zuordnen und auch neue Daten dementsprechend klassifizieren [[Maximum Likelihood Estimation]].

Wir nehmen also in diesem Fall an, dass unsere daten mit einem Gaussian Mixture Model (GMM) generiert wurden. Das entspricht der Summe verschiedener Gauß-Verteilungen.

Um im eindimensionalem die Daten an eine Gaußverteilung zu fitten berechnet man den Mittelwert und die Varianz des Datensatzes und setzt diese in die Gaußverteilung ein. In höheren Dimensionen nutzt man entsprechend einen n-dimensionalen Mittelwert-Vektor und für die Varianz benutzt man die Kovarianzmatrix.

Ähnlich wie beim [[k-means Clustering]] berechnet man die responsibility sets und aktualisiert in jedem Schritt dementsprechend die Parameter.
