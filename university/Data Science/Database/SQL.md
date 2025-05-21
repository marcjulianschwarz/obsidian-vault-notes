---
uni-module: "KonzMod"
---

# SQL

ist eine relationale Anfragesprache.

```SQL
SELECT x
FROM y
WHERE True/False
```

Das Ergebnis von ==SELECT== ist immer eine Multi-Menge. Es werden also keine Duplikate entfernt. Um Duplikate zu eliminieren verwendet man das Stichwort ==DISTINCT==. (vergleichbar mit [[Projektion]] und [[Selektion]] aus der [[Relationenalgebra]])

## Mengenvergleiche

```SQL
WHERE x IN (1, 2, 3)
WHERE x IN (SELECT ...)

WHERE EXISTS (SELECT ...)
```

## Quantoren

```SQL
WHERE x = ANY ()
WHERE x > ALL ()
```

## Join

![[Bildschirmfoto 2021-07-19 um 11.17.23.png]]
![[Bildschirmfoto 2021-07-19 um 11.17.47.png]]
![[Bildschirmfoto 2021-07-19 um 11.17.56.png]]

## Sortierung

```SQL
ORDER BY x ASC, y DES
```

## Mengenoperatoren

In SQL sind auch die gängigen [[Mengenoperationen]] UNION, INTERSECT und EXCEPT verfügbar. Natürlich müssen dafür die Relationen auch vereinigungsverträglich sein.

## Aggregationsfunktionen

- MIN / MAX
- COUNT
- COUNT(DISTINCT)
- AVG / SUM

## Gruppierung

Manchmal möchte man Aggregationsfunktionen nur auf einen Teil einer Spalte anwenden und nicht auf alle Einträge.
Dafür gibt es das Prinzip der Gruppierung. Man teilt dafür die Relation anhand einer Spalte in Gruppen auf und kann dann für jede Gruppe nur den entsprechenden Teil einer Spalte aggregieren.
Das Ergebnis enthält dann nur für jede Gruppe ein Tupel. Deswegen müssen über alle Elemente aggregiert werden, die nicht im GROUP BY Statement stehen.

### HAVING

Mit dem HAVING Statement können Bedingungen auf aggregierte Spalten gestellt werden. Auch hier kann natürlich **nur** auf aggregierte Spalten zurückgegriffen werden.

## Allgemeine Abarbeitung einer SQL Anfrage

![[IMG - SQL Schema.png]]

## Geschachtelte Anfragen

Mit geschachtelten Anfragen können Relationen dynamisch erzeugt werden.

## Einfügen

```SQL
INSERT
INTO Tabelle [Attribute]
VALUES (Werte)
```

Für jedes Attribut, das keinen dazugehörigen Wert in der VALUES Liste hat wird der NULL Wert angenommen.

## Löschen

```SQL
DELETE FROM Tabelle
WHERE Bedingung
```

## Update

```SQL
UPDATE Tabelle
SET Attribut = Wert
WHERE Bedingung
```

## Beispiele

### TOP N Anfrage

```SQL
select count(*)
from table
...
```
