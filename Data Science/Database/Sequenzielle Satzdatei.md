---
alias: [SAM, Sequential Access Method]
---
# Sequenzielle Satzdatei

Anwender will Folge von Sätzen fester oder variable Länge.

Unterstützt:
- sequenzielles schreiben
- sequenzielles lesen

*Nicht* unterstützt: 
- wahlfreies Lesen eines bestimmten Satzes (random access) → das würde sehr lange dauern, da zuerst alle Sätze durchlaufen werden müssen. Deswegen wird diese Funktion gar nicht erst angeboten
- Einfügen eines Satzes 
- Ändern eines Satzes
	- Wäre mit Längenänderung des Satzes verbunden

Schreibreihenfolge wird komplett vom Benutzer definiert.

![[IMG - Sequenzielle Satzdatei.png]]


Sortierung sequenzieller Satzdateien 
[[Stapelverarbeitung]]

## Zugriffsoperationen

- Datei öffnen
	- wie bei [[Datei]]
	- beim schreiben: Satzlänge muss angegeben werden (0 = variabel)
	- beim lesen: Ausgabe Satzlänge
- Nächsten [[Satz]] lesen
	- Satzlänge: maximale Länge (Puffer Größe)
	- Ausgabe: tatsächliche Länge
	- Satzpuffer oder Zeiger werden zurückgegeben
	- Dateikontrollblock (Leseposition) weiterrücken zum lesen des nächsten Satzes
- Nächsten [[Satz]] schreiben
	- bei fester Satzlänge wird die Satzlänge im Parameter ignoriert
	- Fehler
		- [[Satz]] zu lang
		- Datei war zum Lesen geöffnet
		- Kein Platz im Hintergrundspeicher
- Schließen einer Datei
