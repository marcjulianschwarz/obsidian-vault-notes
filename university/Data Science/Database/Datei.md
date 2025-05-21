---
uni-module: IDB

alias: [Dateien]
---

# Datei

Abstrahiert den [[Magnetplattenspeicher]] und alle Details dazu.

- Namen
- lineare Folge an Blöcken
  - sind direkt ansprechbar über eine laufende Nummer
  - wird aber nicht unbedingt linear auf der Platte abgelegt (also kann aus verschiedenen Speicherstellen geholt und zusammengebaut werden)
- Dynamisch erweiterbar um zusätzliche Blöcke (wenn man etwas an eine Datei anfügt, sie durch Daten erweitert)

Die dünnen Linien sind aber unsichtbar für den Anwender. Also Optimierung der unteren Schichten ist möglich ohne eine Änderung an der oberen Schicht.
![[IMG - Datei als Abstraktion.png]]

blockorientierte Zugriffsmethode für eine Datei (access method).
Datei kann mit einem Modus (schreiben, lesen, ergänzen) geöffnet werden.
Durch das Dateisystem können verschiedene Dinge (z.B. auch Kontrollen) eingeführt werden.
Datei wird am Ende wieder geschlossen.
Aktuelle Dateigröße kann ausgelesen werden. Gegenoperation zum Datei ergänzen gibt es auch (drop), gibt Blöcke von hinten aus wieder frei.
Beliebiges Löschen von Blöcken ist nicht möglich.

Zur Verwaltung der ganzen Dateien braucht es eine [[Verwaltungsdatenstruktur]].
