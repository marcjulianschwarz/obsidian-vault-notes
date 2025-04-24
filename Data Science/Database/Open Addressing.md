---
uni-module: "IDB"
---

# Open Addressing

Das Open Addressing ist ein Verfahren um überlaufende [[Buckets|Buckets]] beim [[Gestreute Speicherung|Hashing]] zu umgehen.

Dabei wird auf Nachbar-Buckets in einer festgelegten Reihenfolge ausgewichen.

Also wenn man beim lesen erkennt, dass ein Bucket bereits voll ist, dann weiß man (dank der festgelegten) Reihenfolge genau wo man nach dem Rest suchen muss.

_Vorteile:_

- Es wird kein zusätzlicher Speicher benötigt

_Nachteile:_

- Beim Suchen findet man auch immer Überläufe in den Buckets und nicht nur Treffer
- Beim Löschen müssen Überläufe auch wieder zurückgeholt werden
- Und zuletzt werden die Nachbarn jetzt schneller gefüllt
