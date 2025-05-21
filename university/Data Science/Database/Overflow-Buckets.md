---
uni-module: "IDB"
---

# Overflow-Buckets

Im Gegensatz zu [[Open Addressing]] müssen hier spezielle Überlauf-[[Buckets]] angelegt werden.
Also jeder Block (Primärbucket) hat einen Zeiger auf seinen eigenen Überlaufblock (Überlaufbucket).

_Nachteil:_

- kostet extra Speicherplatz

_Vorteil:_

- Die Sätze werden nicht mehr gemischt
- Die Nachbar-Buckets werden nicht beeinträchtigt
