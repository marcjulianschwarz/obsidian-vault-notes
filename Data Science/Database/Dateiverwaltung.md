---
uni-module: IDB
---
# Dateiverwaltung

[[Schichtenbildung]] durch:

- Hardware (physische Speichergeräte)
- "logische Speichergeräte" mit zum Beispiel Störsicherheit → Durch Programme und Informatik erzeugt (nicht mehr "real")
- [[Datei|Dateien]] (Dateikonzept)
  → Alles abstrahiert das darunter liegende System

→ [[Arten von Datenträgern]]

Erhöhung der Störsicherheit indem man Paritätsfehler und Schreibefehler durch erneutes lesen oder schreiben verhindert.
Ein Ausgabe Prozeduren
[[Gerätetreiber]]

Lösung von fester Größe der Datenträger durch flexible Zuordnung von logischen Geräten (Laufwerken) auf phyische Speicher:

- RAID → Zusammenfassung mehrerer phyischer Speicher zu einem großen logischen Gerät
- Ein physisches Laufwerk in mehrere Platten aufteilen (partitionieren)

## Anwendungsprogramme arbeiten direkt mit Ein Ausgabeschnittstelle

_Vorteile:_

- schnell
- maximale Speicherausnutzung (keine Verwaltungsdaten müssen gespeichert werden)

_Nachteile:_

- Kein Schutz, alles kann von jedem gelesen werden
- Zylinder werden einfach zwischen den Programmen aufgeteilt
  - Reservierung zusätzlichen Speichers
  - Absprache durch Programmierer
- Fehlermöglichkeiten (Überschreibungen)
- starre Aufteilung der Platte, schwierig zu ändern

_Lösung:_
Indirektion durch [[Datei|Dateien]]

## Vorteile und Nachteile

![[IMG - direkter vs. blockorientierter Speicherzugriff.png]]

→ letztendlich sind wir jetzt unabhängig von den Speichergeräten. → Information Hiding

→ [[Datei]] als Basis für weitere Abstraktion.

## Anfang der Schichtenbildung:

![[IMG - Abstraktion Speicherungsstrukturen.png]]
