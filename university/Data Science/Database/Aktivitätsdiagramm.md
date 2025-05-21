---
uni-module: "KonzMod"
---

# Aktivitätsdiagramm

Mit einem Aktivitätsdiagramm kann man Kontroll und Datenflüsse zwischen verschiedenen Aktionen darstellen und Objekt/nicht-Objektorientierte Systeme modellieren.

## Aktivität

Aktivität ist ein anderer Begriff für eine Aufgabe, die mit verschiedenen ==Aktionen== (atomare Bestandteile einer Aktivität) von Menschen oder Maschinen erledigt wird.

[[Gerichteter Graph]] mit Aktivitätsknoten und Kanten. Eine Aktivität kann Eingabe und Ausgabeparameter haben. An Kanten können auch Bedingungen stehen.

### Arten von Knoten

- Aktionsknoten
- Kontrollknoten
- Objektknoten (Ein und Ausgabeparameter)

#### Kontrollknoten

- Inititalknoten -> Beginn
- Fisheye -> Beendet alle Abläufe der Aktivität
- Ablaufendknote -> Beendet nur einen Ablauf
- Entscheidungsknoten mit Bedingung
- Vereinigungsknoten zum zusammenführen alternativer Pfade
- Parallelisierungsknoten
- Synchronisierungsknoten

### Arten von Kanten

- Kontrollflusskanten -> Reihenfolge
- Objektflusskanten -> Weitergabe von Daten oder Objekten

## Beispiel eines Aktivitiätdiagramms

![[Bildschirmfoto 2021-07-20 um 16.47.44.png]]
