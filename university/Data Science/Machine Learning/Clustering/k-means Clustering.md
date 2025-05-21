---
uni-module: EMD
---

# k-means Clustering

Mit dem K-means Clustering Algorithmus lassen sich für einen Datensatz mit einer angegbenen Zahl der Cluster (k), alle Punkte aus diesem Datensatz einem der k Cluster zuweisen.
Bei einigen Daten-Verteilungen funktioniert der k-Means Algorithmus leider nicht besonders gut. Eine Alternative ist daher das [[Gaussian Mixture Expectation Maximization]] Modell.

- The k-means Clustering algorithm only works with continous data, we thus need the k-modes algorithm to work with [[Categorical Data]] where you take the value that occurs most frequently in the data as centroid.
- It can only detect [[Konvexe Menge|convex]] shapes
- It is sensitive to [[Outlier|Outliers]] → one could thus use [[k-medoids Clustering|PAM]] which is insensitive to [[Outlier|Outliers]]

## Algorithmus

1. Partition data into $k$ random / non-empty sets
2. Compute centroids of the clusters
3. For each [[Entity|Data Object]]
   1. Calculate distance to centroid
   2. Pick the one with the smallest distance
   3. Assign object to that centroids cluster
4. If changes were made, repeat.

[[Laufzeit]]: $\mathcal{O}(tkn)$ where $n$ is number of data points $k$ is number of clusters and $t$ is number of iterations. The number of iterations is often really small. Thus more or less linear.
Better than [[k-medoids Clustering|PAM]].

---

5. Cluster zufällig zuordnen
6. Wiederholen bis sich nichts mehr ändert
   1. Für jeden Datenpunkt
      1. Rechne Distanz zu jedem Cluster aus und wähle das Minimum aus
      2. Weise den Datenpunkt diesem Cluster zu
   2. Für jeden Cluster
      1. Berechne das Responsibility Set
      2. Berechne den Durschnitt des Clusters

## Anwendung

→ [[Clustering für Bildbearbeitung]]
