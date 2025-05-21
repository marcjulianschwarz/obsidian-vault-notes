---
uni-module: "KonzMod"
---

# Referenzielle Integrität

bedeutet, dass in einem Fremdschlüssel-Attribut nur Werte vorkommen dürfen, die es auch im referenzierten Primärschlüsselattribut wirklich gibt.
Wenn ein Fremdschlüssel im DBMS als ein solcher markiert wird, dann garantiert das DBMS, dass die referenzielle Integrität nicht verletzt wird.
Außerdem kann dem DBMS mitgeteilt werden, was zu tun ist, wenn ein Eintrag geändert oder gelöscht wird.
Man kann die Aktion ablehnen mit ==RESTRICTED==, alle referenzierednen Tipel auch ändern mit ==CASCADES==, alle Referenzen auf NULL setzen mit ==NULLIFY== oder mit ==SET DEFAULT== auf einen Standardwert zurücksetzen.
Diese Integritätsbedingungen können beim erstellen einer Tabelle angegeben werden (-> [[SQL]]).
