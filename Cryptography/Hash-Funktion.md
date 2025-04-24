---
uni-module: "IDB"
---

# Hash-Funktion

Eine Funktion, die beliebig lange Zeichenketten in eine Zeichenkette mit fest vorgegebener Länge umwandelt.

- [[Alphabet]]
- Wörter der Länge $m$ aus dem Alphabet $\Sigma^m$
- die Menge aller möglichen Wörter aus dem Alphabet $\bigcup_{m \geq 0} \Sigma^m$

Eine Hashfunktion ist dann eine Abbildung der Form
$$h: \Sigma^* \rightarrow \Sigma^n.$$

Für kryptographische Zwecke möchte man noch mehr Eigenschaften haben, deswegen spricht man dann von **kryptographischen Hash-Funktionen**, wenn folgende Eigenschaften erfüllt sind:

1. Für jede Zeichenkette $a$ soll der Hashwert $h(a)$ schnell berechnet werden können.
2. Zu einem Hashwert soll man praktisch nicht die ursprüngliche Zeichenkette berechnen können → **Einwegfunktion**
3. Man findet praktisch keine unterschiedliche Zeichenketten mit dem selben Hashwert (stark kollisionsresitstent)

Stark kollisionsresitstent → schwach kollisionsresitstent

Eine Hashfunktion der oben beschriebenen Form ist nie injektiv. Wenn die Länge des Hashes $n$ ist und wir eine Folge an Zeichenketten mit $k$ Elementen verwenden, dann ist die Wahrscheinlichkeit eine Kollision zu finden größer als 99% wenn
$$k \geq 3.1 \sqrt{\left|\Sigma^n\right|}=3.1|\Sigma|^{n / 2}$$
ist.
In der Praxis sollte der Hash daher möglichst groß sein um es unmöglich zu machen eine Kollision zu finden.

## Beispiele Hashfunktion

- [[Secure Hash Standard|SHA-1]]

## Aus IDB

- Möglichst gleimäßige [[Wahrscheinlichkeitsmaß|Verteilung]] auf [[Buckets]]
- Kollisionen sind erlaubt und teilweise auch erwünscht

### Auswahl der Hash-Funktion

hängt vom Typ des Schlüssels und der [[Wahrscheinlichkeitsmaß|Verteilung]] der Werte ab.
Je genauer die [[Wahrscheinlichkeitsmaß|Verteilung]] bekannt ist desto besser kann man die Hash-Funktion mache n.
Z.b.: Kundenummer: erste zwei Ziffern sind gleich, also nur den Rest verwenden.

Wenn man nichts über die Schlüssel weiß kann man das [[Divisions-Rest-Verfahren]] verwenden.

### Überlaufbehandlung

Leide ist eine völlig gleichmäßige [[Wahrscheinlichkeitsmaß|Verteilung]] nicht immer möglich. Das kann dazu führen, dass ein Bucket überläuft, also kein Platz mehr für alle Sätze vorhanden ist.

Eine Lösung dafür wäre zum Beispiel [[Open Addressing]].
Eine zweite Möglichkeit ist [[Overflow-Buckets]].

Allerdings hat man bei beiden Verfahren den Nachteil, dass man ab sofort zwei Blockzugriffe braucht um auf Daten zuzugreifen.

### Hashberechnung

Daten werden erstmal über eine bestimmte Bit-Länge gefaltet und zum Beispiel mit XOR zusammengerechnet.
Erst danach wird das [[Divisions-Rest-Verfahren]] verwendet. (damit die Zahlen für die Division nicht zu groß sind).
