---
uni-module: "KRY"

alias: "ECB-Modus"
---

# Electronic-Codebook-Modus

So läuft beispielsweise die beschriebene [[ALBC-2-Verschlüsselung]].

Einfachste Art eine [[Blockchiffre]] durchzuführen. Dabei wird ein Text in Blöcker der Länge $k$ eingeteilt und der i-te Block wird mit der Verschlüsselungsfunktion verschlüsselt. Die Entschlüsselung funktioniert äquivalent mit der Entschlüsselungsfunktion (inverse der Verschlüsselungsfunktion).

Ein **Nachteil**, der dabei entsteht ist, dass Regelmäßigkeiten des Klartextes auch im verschlüsselten Text sichtbar sind. Das würde natürlich beim entschlüsseln helfen.
