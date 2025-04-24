---
uni-module: "KonzMod"

alias: "Aggregation Type"
---

# Aggregationstypen auf MDMs

1.  beliebig aggregierbar (Sales, Turnover, ... ): FLOW
2.  nicht temporal summierbar (Stock, Inventory, ... ): STOCK
3.  nicht summierbar (Preis, Steuer, i.Allg. Faktoren): VPU (Value per Unit)

## Aggregationsoperatoren

SUM, AVG, MIN, MAX, COUNT
aber auch
cumulating() oder ranking(Top(N))

Aber Achtung: Nicht alles Funktionen können überall sinnvoll angewendet werden.

MIN, MAX und AVG darf immer verwendet werden.

## Sample Aggregation: SUM

![[Bildschirmfoto 2022-10-10 um 20.22.16.png]]
