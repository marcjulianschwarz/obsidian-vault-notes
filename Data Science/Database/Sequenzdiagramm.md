---
uni-module: "KonzMod"
---

# Sequenzdiagramm

## Interaktionen

Abfolge von Ereignisspezifikationne, die einen potentiellen Ereigniseintritt zur Laufzeit definieren.

Eine Folge von konkreten Ereigniseintritten heißt ==Trace==.
Eine Ausführungsspezifikation wird mit einer ==Start und Endereignisspezifikation== gekennzeichnet. In diesem Abschnitt wird etwas entweder indirekt ausgeführt (weiß) oder direkt ausgeführt (schwarz).

## Nachrichtentypen

- synchron: Der Sender wartet bis die Interaktion beendet ist
- asynchron: Der Sender wartet auf keine Antwort
- Nachrichten können an einen unbekannten Ort gehen und gelten dann als lost
- Nachrichten können aus einem unbekannten Ort gefunden werden und gelten dann als found

![[IMG - Sequenzdiagramm.png]]

## Kombinierte Fragmente

Dursch Schachtelung von Teil-Sequenzdiagrammen mithilfe verschiedener Operatoren, können komplexere Kontrollstrukturen dargestellt werden.

### Operatoren

- [[alt-Operator]]
- [[opt-Operator]]
- [[break-Operator]]
- [[loop-Operator]]
- [[seq-Operator]]
- [[strict-Operator]]
- [[par-Operator]]
- [[critical-Operator]]
- [[ignore-Operator]]
- [[consider-Operator]]
- [[assert-Operator]]
- [[neg-Operator]]

### Interkationsreferenzen

Sie dienen der Referenzierung anderer Sequenzdiagramme innerhalb eines Sequenzdiagramms. Dadurch kann man Teile wiederverwenden und Diagramme modularisieren.
Mit dem Wort ==ref== kann innerhalb eines Sequenzdiagramms auf ein anderes Modul/Fragment verwiesen werden.

Mit Start und Zielmarken können **goto** ähnliche Sprungstellen erstellt werden.

![[IMG - Ziel Start Marken.png]]

Mit Hilfe von ==Verknüpfungspunkten== können mehrer Sequenzdiagramme verbunden werden. Dafür werden die vorher als lost und found bezeichneten Stellen verwendet.

![[IMG - ref operator.png]]
