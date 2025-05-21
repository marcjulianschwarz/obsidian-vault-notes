
# Blockung

Normalerweise passen mehrere Sätze in einen Block, da Sätze typischerweise 100 - 1000 Bytes lang sind. EIn Block kann unterschiedlich viele Sätze enthalten. In manchen Fällen ist es auch möglich, dass ein [[Satz]] über mehrere Blöcke geht (spanned records).

![[IMG - Sätze im Block.png]]

- Feste Satzlänge
	- Sonderfall
	- kein Längenfeld (Infos über die Länge eines Satzes) nicht mehr nötig
	- feste Anzahl von Sätzen pro Block → bessere Effizienz
	- aber: ungenutzter Speicher am Ende eines Blocks
- Variable Satzlänge
	- Anzahl der Sätze ändert sich von Block zu Block
	- [[IMG - Menge an Sätzen.png]] → Man kann also die Sätze umsortieren bis nur noch wenig ungenutzter Speicher am Ende der [[Datei]] übrig ist.

Welche der beiden Möglichkeiten benutzt wird ist eine Eigenschaft der [[Datei]]. Wir haben ab sofort also Satzorientierte-Dateien, die entweder feste oder variable Satzlängen haben.


