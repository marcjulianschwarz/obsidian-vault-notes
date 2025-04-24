---
uni-module: "KonzMod"
---

# XML

Semistrukturierte Daten wie in [[Datenbank|Datenbanken]] lassen sich nur schwer austauschen. XML bietet dafür eine Lösung, da sich die Daten darin selbst mit [[Metadaten]] beschreiben.

Damit XML Dokumente einheitlich und untereinander gut vergleichbar sind muss immer darauf geachtet werden, dass [[Wohlgeformtheit]] und [[Gültigkeit]] eines XML Dokumentes nicht verletzt werden.

**Aufbau**

1. Prolog
2. [[Document Type Definition]]
3. Root element -> elements

**Namensräume**
Mit Namensräume können Vokabulare importiert werden. Mit _xmlns:Kürzel_ oder ohne Kürzel. Der Namensraum bezieht sich auf die Unterelement des Elements, in dem er definiert wurde.

**Verweise zwischen und in XML Dokumenten**

- [[Xlink]]
- [[Xpointer]]

**DTD vs XML-Schema**

- [[Document Type Definition]]
  - streng hierarchisch
  - eigene Syntax
  - wenige Datentypen
  - Referenzierung mit IDREF ist nur eingeschränkt möglich
- XML-Schema
  - flexibler
  - Typen werden direkt mit XML definiert
  - [[Xpointer]] und [[Xlink]] für komplexe Verweise

## Addresierung

XML Dokumente werden als [[Baum]] mit verschiedenen Knotentypen interpretiert. Der Wurzelknoten ist ein zusätzlich generiertes Element, welches die Dokumentwurzel als Kind besitzt. Danach kommen die Elementknoten. Attribute und Text werden ebenfalls als einzelne Knoten wahrgenommen.
Zusätzliche Knoten sind

- Verarbeitungsanweisungsknoten
- Kommentarknoten
- Namensraumknoten.

Eine Sprache um Anfragen an diese Baumstruktur zu machen ist [[XPath]].

## Entitäten

Entities sind seperate Dateneinheiten, die vor der Validierung aufgelöst werden. Sie können in der [[Document Type Definition]]definiert werden. Sie werden mit einem & Zeichen gekennzeichnet.

## Bedeutung von XML

XML ist textbasiert und damit leicht zu erstellen und auch ohne technische Mittel gut lesbar. Anwendungen können durch Tags automatiesiert nur Teile eines Dokuments lesen.

XML Daten können leicht durch Stylesheets (XSL) präsentiert werden.
Außerdem ist XML sehr leicht wiederverwendbar. Dokumente können modularisiert werden und durch Redundanzfreiheit kann das Datenvolumen reduziert werden.

Durch die bereits besprochenen Referenzierungsmethoden können Links zwischen Dokumenten und Inhalten leicht hergestellt werden.
