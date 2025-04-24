---
uni-module: "KonzMod"
---

## XPath Ausdrücke

Mit XPath Ausdrücken kann man von einem bestimmten Knoten aus den [[XML]]-Baum durchlaufen und somit Anfragen formulieren.
Inhalte werden immer als eine der folgenden Knotenarten dargestellt:

- Wurzelknoten
  - Wird zusätzlich zum Dokumentknoten erstellt
  - Der Dokumentknoten ist also ein Kind des Wurzelknoten
- Elementknoten
- Attributknoten
- Textknoten
- Verarbeitungsanweisungsknoten
- Kommentarknoten
- Namensraumknoten

Ein solcher Pfad kann direkt angegeben werden. Auf die Ergebnismenge kann dann wie auf einen Array zugegriffen werden. Mit einem "//" können alle Elemente die dem Ausdruck entsprechen selektiert werden, egal auf welche Ebene/Tiefe.
Allerdings kann man auch mittels relativer Navigation den Baum durchlaufen. Dafür benutzt man Achsen:

- child::
- self::
- descendant::
- descendant-or-self
- parent::
- ancestor::
- ancestor-or-self::
- preceding::
- preceding-sibling::
- following::
