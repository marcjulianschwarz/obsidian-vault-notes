---
uni-module: "KonzMod"
---

# Verbund

Beim Verbund wird mithilfe des [[Kreuzprodukt]] eine Menge an Tupeln aus zwei Relationen aufgespannt, von welcher dann mit einem Prädikat eine Teilmenge mithilfe von [[Selektion]] gebildet wird.
Formal wird der Verbund so definiert, allerdings wird das so niemals realisiert, da das [[Kreuzprodukt]] viel zu groß ist. Stattdessen kann einfach mit zwei Schleifen über die Tupel iteriert werden um Verbund Partner zu suchen.
In [[SQL]] ist der Verbund vergleichbar mit dem ==JOIN ON== Statement.

![[Bildschirmfoto 2021-07-19 um 10.14.27.png]]

Wenn nach links oder rechts von diesem Symbol noch zwei Strich ausgehen, dann ist das ein rechter oder linker äußerer Verbund. Es werden also alle Tupel mitgenommen, die auf der jeweiligen Seite keinen Partner gefunden haben.

![[Natürlicher-Verbund]]
![[Auto-Join]]
