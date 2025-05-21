
# Clustering mit Kruskal
Wenn man den Kruskal [[Algorithmus]] nicht komplett bis zur letzten Iteration durchläuft, kann man ihn auch als Clustering Algorithmus verwenden. Bei jeder Iteration werden zwei disjunkte Teilbäume miteinander verbunden. Wenn man jetzt also eine Iteration früher aufhört bleiben zwei disjunkte Teilbäume übrig. Genauso geht das auch mit mehr Clustern. Man muss dann nur eben zwei oder mehr Iterationen früher aufhören.
Weil man beim Kruskal Algorithmus immer mit den kleinsten Kanten anfängt entstehen so Cluster, in welchen der Abstand der Datenpunkte möglichst gering ist.