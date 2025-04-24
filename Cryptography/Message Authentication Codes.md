---
uni-module: "KRY"

alias: "MAC"
---

# Message Authentication Codes

Mit einer [[Hash-Funktion]] lässt sich überprüfen ob zwei Nachrichten den gleichen Inhalt enthalten beziehungsweise ob eine Nachricht verändert wurde.
Will man aber die Authetizität einer Nachticht überprüfen verwendet man sogenannte Message Authentication Codes.

Diese können zum Beispiel so funktionieren, dass der Hashwert bevor er verschickt wird mit einem [[Schlüssel]] verschlüsselt wird. Ein Angreifer kann zwar die Werte der Datei verändern, das fällt aber spätestens dann auf, wenn versucht wird die Datei mit dem Schlüssel zu entschlüsseln (das wird fehlschlagen).
