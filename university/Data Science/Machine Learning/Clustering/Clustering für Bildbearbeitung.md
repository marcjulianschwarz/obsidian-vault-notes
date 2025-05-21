---
uni-module: DSFI
---

# Clustering für Bildbearbeitung

Bilder können mit einer Histogrammanalyse und einer Thresholding Funktion segmentiert und komprimiert werden.

Das ganze funktioniert allerdings noch besser, wenn man zum Beispiel [[k-means Clustering]] verwendet um ähnliche Bereiche in einem Bild zu erkennen. Da dieser Algorithmus allerdings nicht sehr robust gegenüber Rauschen in der Bilddatei ist lohnt es sich das Chan-Vese Segmentierungsverfahren zu verwenden. Dieses Verfahren besteht aus dem K-Means Algorithmus und bestraft zusätzlich Ausreißer (Regulierungsterm), was es robust gegen Rauschen macht.
