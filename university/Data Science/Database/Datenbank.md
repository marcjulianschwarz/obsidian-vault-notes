---
uni-module: "KonzMod"

alias: "Database"
---
# Datenbank

> [!NOTE] Definition
> A database is a collection of related data.
>
> Eine Datenbank repräsentiert einen Ausschnitt der realen Welt, auch Miniwelt genannt. Sie hat einen Zweck und ist für eine Benutzer und Anwendungsgruppe als Zielgruppe entworfen.

- [[Datenunabhängigkeit]]
- Außerdem muss die [[Datenbank]] neutral gegenüber Anwendungen sein. Sie darf also nicht auf eine spezielle Anwendung zugeschnitten sein sondern sollte möglichst wiederverwendbar sein.

> [!Check] Pros
>
> - Redundanzfreiheit durch kontrollierte und zeitgerechte Änderungen
> - Vermeidung von Inkonsistenzen und privaten Dateien
> - Zentrale Kontrolle der Datenintegrität
>   - Zugriffskontrollen
>   - logische und physische Datenintegrität
> - Mehrbenutzerbetrieb durch Transaktionssysteme
> - hohe Fehlertoleranz selbst bei physischen Einwirkungen
> - Performant
> - Skalierbar
> - Flexibel

> [!Warning] Cons
>
> - Overhead durch [[DBMS]] (initial und fortwährend)
> - General Purpose Anwendung, Spezialisierung nur schwer möglich
> - Macht erst bei sehr vielen Daten sind
> - Nicht für Echtzeitanforderungen ausgelegt

![[Datenbank 2023-07-29 15.47.19.excalidraw]]

Ein Datenbankmodell ist eine Strukturierungsvorschrift für Daten. Ein Beispiel hierfür wäre eine Tabellenform.
Das Datenbankschema hingegen beschreibt eine konkrete Datenbank. Also die Attribute, etc.

Eine Datenbank beinhaltet auch immer [[Metadaten]].

[[Schema-Architektur ANSI SPARC]]

## Datenmodellierung

![[IMG - KonzMod Overview.png]]

Es gibt viele verschiedene **Typen von Datenbanksystemen:**

- Hierarchisch
- [[Flussnetzwerk|Netzwerk]]
- [[Relationenmodell]]
- Objektorientiert
- Objektrelational
- [[XML]]
- NoSQL
- RDF Triple Stores

