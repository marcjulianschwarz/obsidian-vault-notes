---
uni-module: "IDB"

tags: "MOC"
---

# MOC - Implementierung von Datenbanksystemen

## Dateiverwaltung

Beim implementieren eines [[DBMS]] muss immer die [[Datenunabhängigkeit]] gewährleistet werden. Die Software sollte also möglichst eine [[Generische Software]] sein. Um das umsetzen zu können benötigt man [[Schichtenbildung]] wobei der physische Speicher durch mehrere [[Schicht | Schichten]] abstrahiert wird. Realisiert wird das ganze durch die [[Dateiverwaltung]].

Für den physischen Speicher gibt es verschiedene [[Arten von Datenträgern]] mit jeweils anderen Vor- und Nachteilen:

- [[Magnetbandspeicher]]
- [[Optische Speicher]]
- [[Flash Speicher]]
- [[Magnetplattenspeicher]]

### Magnetplattenspeicher

Für uns ist vor allem der Magnetplattenspeicher wichtig. Um dort Daten abzulegen oder aufzurufen muss man die Daten über den [[Zugriffskamm]] lokalisieren. Dafür muss man im entsprechenden [[Zylinder]] die richtige [[Spur]] auswählen, in welcher es viele [[Slot | Slots]] gitb die einen [[Block]] enthalten oder aufnehmen können.

Damit sich die Anwendungen nicht alle mit dieser Struktur auseinandersetzten müssen wird sie durch die [[Datei]] abstrahiert. Natürlich müssen die Dateien auch verwaltet werden. Dafür gibt es die [[Verwaltungsdatenstruktur]].

Im [[Hauptspeicher]] sind alle aktuell laufende Programme. [[Gerätetreiber]]

## Sätze

Ein Block hat immer die gleiche vom System vorgegebene Größe. Will man eine varible Länge haben kann man einen [[Satz]] verwenden. Trotzdem basiert der Satz noch auf Blöcken ([[Blockung]]). Durch eine [[Satzadresse]] ist ein Satz direkt ansprechbar. Nur in dem Sonderfall einer [[Sequenzielle Satzdatei | Sequenziellen Satzdatei]] ist dieses wahlfreie Lesen nicht mehr möglich.

[[Freispeicherverwaltung]]

### TID-Konzept

Mit dem [[TID-Konzept]] kann man Satzadressen realisieren. Die [[Struktur eines Blocks im TID-Konzept]] besteht aus Datensätzen und dem [[Positionsindex]], der die Positionen der Sätze innerhalb eines Blockes beschreibt.
Durch die [[Operationen des TID-Konzept]] könne Sätze hinzugefügt, verlängert, gelöscht oder verschoben werden.

[[Puffer]]

## Schlüsselzugriff

[[Satzadresse | Satzadressen]] sind sehr künstlich. Möchte man zum Beispiel einen oder all Sätze bzw einen Teil des Satzes mit einem bestimmten Inhalt finden tut man sich damit sehr schwer.
Deshalb führt man für diese Inhalte einen Suchschlüssel ein.

Die [[Sequenzielle Satzdatei]] oder auch **direkte Satzdatei** kann das noch nicht. Die Möglichkeit danach zu suchen wäre einen sequenziellen **Scan** zu machen. Das ist aber sehr umständlich und ineffizient.
Es muss also eine neue Hilfsstruktur her.

Eine Möglichkeit einen solchen Schlüsselzugriff umzusetzen ist die [[Gestreute Speicherung]] wobei eine [[Hash-Funktion]] verwendet wird um die Daten auf verschiedene [[Buckets]] aufzuteilen. Eine solchne Funktion wäre zum Beispiel das [[Divisions-Rest-Verfahren]].

Nur der Administrator kann die Hash-Funktion ändern. Damit ist eine Reorganisation des Datenbstands möglich.

Operationen:

- `HashedRecordFile::insert(char: RecordBuffer, RecordLength, KeyValue)`
- `HashedRecordFile::read(char: KeyValue, int RecordLength)`
- modify, delete, read-first, read-next
- modify-key

Alle Operationen laufen jetzt nicht mehr über die Satzadresse sondern über den Schlüsselwert.

Vorteile:

- schneller Zugriff

Nachteile:

- Sätze durcheinander
- Speicherplatz muss vorher belegt werden
- Geht nur mit einem Schlüssel → sequenzielle Suche kann passieren, wenn der Schlüssel nicht wirlich eindeutig ist

[[Virtuelles Hashing]]
