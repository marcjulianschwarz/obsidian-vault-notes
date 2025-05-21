---
uni-module: IDB
---

# Magnetplattenspeicher

Hat eine feste Struktur durch [[Zylinder]], [[Slot|Slots]] und [[Spur|Spuren]]. Außerdem hat er eine feste Größe und man hat einen wahlfreien (direkten) Zugriff auf einen Slot-Inhalt. Asynchrone Ein- und Ausgaben möglich.

## Aufbau

- [[Block]]
- [[Slot]]
- [[Spur]]
- [[Zylinder]]
- [[Zugriffskamm]]

![[IMG - Aufbau Plattenspeicher.png]]

_Adressierung von Daten:_
Gerätenummer → Zylindernummer → Spurnummer → Slotnummer → Daten
Diese Adressierung wird natürlich abstrahiert.

Physische Adressierung:
![[IMG - readBlock Pseudocode.png]]
![[IMG - writeBlock Pseudocode.png]]
