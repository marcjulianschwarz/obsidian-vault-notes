---
uni-module: IDB

alias: [Blöcke]
---

# Block

Ein Block ist eine Bytefolge mit fester Länge. Solch ein Block bildet die elementare Einheit des Transports zwischen Platte und [[Hauptspeicher]]. Man muss immer mindestens einen Block schreiben. Man kann also nicht nur einen halben Blocken schreiben.

Die Größe von einem Block wird durch das System vorgegeben. Typisch sind 512 Bytes, 2K, 4K. Was aber wichtig ist, ist dass die Größe _fest_ ist. Dadurch entstehen je nach Anwendung Vorteile oder Nachteile:

- Kleine Böcke: man braucht viele E/A-Operationen um größere Datenmengen zu speichern
- Große Blöcke: oft werden uninteressante Daten mitgelesen, die im selben Block gespeichert wurden oder man verschwendet viel Platz, wenn man den Rest im Block leer lässt.

Um dieses Problem zu lösen braucht man eine neue Abstraktion → [[Satz]]
