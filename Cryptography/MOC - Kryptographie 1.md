---
tags: MOC
uni-module: KRY
---

# MOC - Kryptographie 1

## Einführung und klassische Chiffrierverfahren

> [!TIP]- Grundidee der Kryptographie
>
> - Eine Nachricht auf der Seite des Senders transformieren.
> - Die transformierte Nachricht verschicken
> - Die transformiterte Nachricht auf der Seite des Empfängers entschlüsseln.
> - Wichtig ist, dass ein Angreifer die transformierte Nachricht nicht entschlüsseln kann

> [!TIP]- Elemente die zur Verschlüsselung notwendig sind
> [[Klartext]] > [[Kryptosystem]] > [[Alphabet]] > [[Schlüssel]]

### Verfahren

- [[Blockchiffre]]
  - [[Substitutionsverfahren]].
    - [[MASC-Verschlüsselung]]
      - [[CAESER Verschlüsselung]]
  - [[Transpositionsverfahren]]
    - [[TRANSMAT-Verschlüsselung]]
    - [[TRANSSPA-Verschlüsselung]]
- [[Electronic-Codebook-Modus|ECB-Modus]]
- [[Cipherblock-Chaining-Modus|CBC-Modus]]
- Padding

- [[STROM-Verschlüsselung]]
  - [[Vernam-Cipher]]
  - [[AUTOKEY-Verschlüsselung]]
  - [[VIGENERE-Verschlüsselung]]
    - [[Kasiski-Test]]
- [[PLAYFAIR-Verschlüsselung]]
- [[Drehraster-Verschlüsselung]]
- [[Homophone Substitutionsverschlüsselung]]
- [[ADFGVX-Verschlüsselung]]

- [[Kryptanalyse]]
  - [[Ciphertext-only-Angriff]]
  - [[Known-plaintext-Angriff]]
  - [[Chosen-plaintext-Angriff]]
  - [[Häufigkeitsanalyse in der Kryptographie]]

[[Modulo]]

## Kapitel 3 - Grundeigenschaften der Ringe $\mathbb{Z}$ und $\mathbb{Z}/n \mathbb{Z}$

[[O Kalkül|Landau Symbole]]

[[b-adische Darstellung]]

[[Integritätsring]]
[[Modulo]]
[[Euklidischer Ring]]
[[Teilbarkeit]]
[[Primzahl]]
[[Fundamentalsatz der Arithmetik]]

[[Naives Faktorisierungsverfahren]]

Wir definieren die gemeinsamen Teiler von $m$ und $n$ als die Menge an Zahlen $d$, die sowohl $n$ als auch $m$ teilen.
Wir sehen daraus sofort, dass die gemeinsamen Teiler von $m$ und $0$ alle Teiler von $m$ sind und mit $1$ nur $+,-1$, da man $1$ eben nur mit $+1$ und $-1$ teilen kann.
Wenn eine Primfaktorzerlegung leicht zu berechnen ist, dann lassen sich auch schnell alle gemeinsamen Teiler bestimmen indem man alle möglichen Zerlegungen mit Exponenten macht, die kleiner gleich der Exponenten aus der ursprünglichen Zerlegung sind.

Mit dem [[Größter Gemeinsamer Teiler]] könenn wir auch feststellen ob zwei Zahlen [[Teilerfremd]] sind.

Genauso lassen sich gemeinsame Vielfache und das [[Kleinstes Gemeinsames Vielfaches]] definieren.

Der [[Euklidischer Algorithmus|euklidische Algorithmus]] kann den [[Größter Gemeinsamer Teiler|ggT]] bestimmen ohne explizit eine Primfaktorzerlegung berechnen zu müssen.
Wir verwenden die [[Fibonacci-Zahlen]] um zu zeigen wie die [[Laufzeit]] des Algorithmus ist.

Wir wissen, dass die Gleichung
$$ggT(a,b)=ax+by$$mit dem [[Erweiterter Euklidischer Algorithmus|erweitertem euklidischen Algorithmus]] lösbar ist. Wir wollen diese Aussage nun verallgemeinern indem wir zeigen wie wir Lösungen für die Gleichung
$$ax+by=c$$
finden können.

Wenn $ggT(a,b)|c$ und $au+bv=ggT(a,b)$ gilt, dann sind die Lösungen der oben genannten Gleichung:
$$\{(x, y) \in \mathbb{Z} \times \mathbb{Z}: a x+b y=c\}=\left\{\left(\frac{c}{\operatorname{ggT}(a, b)} u+\frac{b}{\operatorname{ggT}(a, b)} m, \frac{c}{\operatorname{ggT}(a, b)} v-\frac{a}{\operatorname{ggT}(a, b)} m\right): m \in \mathbb{Z}\right\}.$$

Diese können in [[Python]] zum Beispiel mit dem EEA wie folgt berechnet werden:

````python
a, b, c = 12345, 987, 9
ggt, u, v = eea(a, b)

if c % ggt == 0:
    for m in range(0, 10):
        x = c / ggt * u + b / ggt * m
        y = c / ggt * v - a / ggt * m
        print(f"{a} * {x} + {b} * {y} = {c}", end="\t -> ")
        print(a * x + b * y == c)```


[[Kongruenz]] ist ein hilfreiches Konzept in der Zahlentheorie.

[[Modulo Invertierbarkeit]]


[[Eulersche Funktion]]


Wir wollen nun die [[Modulo Invertierbarkeit]] verallgemeinern, indem wir Lösungen für die Gleichung
$$ax\equiv b \bmod m$$
suchen. Dabei entspricht die Version mit $b=1$ der normalen Invertierbarkeit.

Gilt
$$ggT(a,m)|b$$
, dann ist die Gleichung lösbar und
$$x_0=\frac{b}{ggT(a,m)}u$$
erfüllt die Gleichung.

Gilt zudem
$$ax_0\equiv b \bmod m$$
, dann gilt außerdem
$$ggT(a,m)|b$$
und es gibt
$$ggT(a,m) \bmod m$$
verschiedene Lösungen der Form
$$x_0+i \frac{m}{\operatorname{ggT}(a, m)} \quad \text { für } \quad i=0, \ldots, \operatorname{ggT}(a, m)-1.$$

Eine beispielhafte Implementierung in [[Python]]

```python
a = 6
b = 4
m = 10
ggt, u, v = eea(a, m)

if b % ggt == 0:
    x0 = b / ggt * u
    if a*x0 % m == b % m:
        for i in range(0, ggt):
            print((x0 + i * m / ggt) % m)
````

Der [[Chinesischer Restsatz|Chinesische Restsatz]] kann verwendet werden um ein Kongruenzgleichungssystem zu lösen.

[[Algorithmus zur Berechnung der abgerundeten Wurzel]]

## Kapitel 4 - Primzahltests

Wir wollen in diesem Kapitel zwei Grundprobleme lösen:

- Überprüfe ob eine große Zahl eine [[Primzahl]] ist
- Konstruiere eine [[Primzahl]] einer bestimmten Größenordnung (mit bestimmten Eigenschaften)

Wir wollen also zum Beispiel eine Primzahl der Gestalt $10^{1000}+r$ konstruieren.

Wir verwenden die [[Eulersche Funktion]] um die Zahlen in einem Intervall zu bestimmen, die keine kleinen Teiler haben.
Damit können wir große Zahlen bestimmen, die so gut wie keine kleinen Teiler haben und somit wahrscheinlich [[Primzahl|Primzahlen]] sind.
Das heißt uns fehlt jetzt nur noch die Möglichkeit zu bestimmen ob diese Zahlen wirklich alles prim sind.

Für eine [[Primzahl]] $p$ und ganze Zahlen $a,b$ gilt:
$$(a+b)^p \equiv a^p+b^p \bmod p.$$

Wir nutzen dieses Lemma um den [[Kleiner Satz von Fermat|Kleinen Satz von Fermat]] zu beweisen. Dieser lässt sich auch aus dem [[Satz von Euler]] herleiten.

Mit dem [[Satz von Euler]] können wir außedem folgende Folgerung zeigen. Wenn $ggT(n,a)=1$, dann gilt
$$x \equiv y \bmod \varphi(n) \quad \Longrightarrow \quad a^x \equiv a^y \bmod n.$$
Durch $x$ und $y$ faches potenzieren von $a$ verschwindet also die eulersche Funktion.

Wir wissen jetzt also

$$
\begin{aligned}
n \operatorname{prim} & \Longrightarrow a^{n-1} \equiv 1 \bmod n \\
a^{n-1} \not\equiv 1 \bmod n & \Longrightarrow n \text { zusammengesetzt }
\end{aligned}
$$

und können damit ausschließen, dass $n$ eine [[Primzahl]] ist, wenn wir ein $a$ finden, sodass
$$a^{n-1} \not \equiv 1 \bmod n.$$
Um diese Überlegung als Primzahltest auszunutzen müssen wir die Potenz sehr schnell berechnen können.
Wir nutzen die binäre Darstellung des Exponenten aus und kommen somit auf die [[Square-And-Multiply-Methode zum Potenzieren]].

Mit dem [[Fermat-Test]] lassen sich [[Primzahl|Primzahlen]] und [[Pseudoprimzahl|Pseudoprimzahlen]] bestimmen beziehungsweise testen.

Spezialfall: [[Carmichael-Zahl]] mit [[Korselt-Kriterium]].

Dieser ungünstige Spezialfall führt uns auf den [[Miller-Rabin-Primzahltest]].

## Exkurs: Sieb des Erathosthenes

[[Sieb des Erathosthenes]]

## Kapitel 5 - Public-Key-Verschlüsselung - RSA

[[RSA]] ist ein Verschlüsselungsverfahren bei dem der Schlüsselaustausch sehr sicher ist, da ein [[Address|Public Key]] von jedem gesehen werden darf, während der [[Private Key]] bei einem selbst bleibt.

**Angriffe auf RSA**

Der RSA-Exponent ist Teil des [[Address|Public Key]]. Wird ein zu kleiner Exponent, von mehreren Personen gleichzeitig verwendet kann man bei Kentniss des Public Key und des Chiffretext diesen mit dem [[Chinesischer Restsatz|Chinesischen Restsatz]] entschlüsseln.

Bei drei Personen mit $e_i=3$ wird der [[Klartext]] zum Beispiel so verschlüsselt
$$b_{1, i}=a_i^3 \bmod N_1, \quad b_{2, i}=a_i^3 \bmod N_2, \quad b_{3, i}=a_i^3 \bmod N_3.$$
Man berechnet mit dem chinesischen Restsatz

$$
c_i \equiv\left\{\begin{array}{l}
b_{1, i} \bmod N_1 \\
b_{2, i} \bmod N_2 \\
b_{3, i} \bmod N_3
\end{array}\right.
$$

Und erhält die Ausgangsfolge mit
$$a_i=\sqrt[3]{c_i}$$

[[Algorithmus zur Berechnung der abgerundeten k-ten Wurzel]]

[[Fermat-Faktorisierung]]

## Exkurs: Kettenbrüche

[[Kettenbruch]]
[[Kettenbruchentwicklung]]

[[Näherungsbruch]]

Approximation irrationaler Zahlen

## Kapitel 6 - Die Pollardsche rho-Methode zur Faktorisierung

[[Pollardsche Rho-Methode]]

## Kapitel 7 - Kryptographische Anwendung diskreter Logarithmen

Wir definieren die [[Ordnung]].

Exkurs zur Funktion

[[Primitivwurzel]]

[[Diskreter Logarithmus]]

[[Schlüsselaustausch nach Diffie-Hellmann]]

[[ElGamal-Verschlüsselung]]
[[Massey-Omura-Verschlüsselung]]

## Kapitel 8 - Kryptographische Hashfunktionen

Ein Beispiel einer [[Hash-Funktion]] ist [[Secure Hash Standard|SHA-1]]. Eine typische Attacke auf Hash-Funktionen ist die Geburtstagsattacke, welche die Eigenschaft ausnutzt, dass Hash-Funktionen nie komplett injektiv sind.
[[Message Authentication Codes]] sind spezielle Hashfunktionen mit denen man die Authentizität einer Nachricht überprüfen kann.

## Kapitel 9 - Digitale Signaturen

Eigenschaften, die eine Signatur haben sollte:

- authentisch
- fälschungssicher
- nicht wiederverwendbar
- Das Dokument ist unveränderbar nach Unterzeichnung
- Die Unterschrift kann nicht zurückgenommen werden

**Allgemeine Verfahren:**

- [[Public-Key-Verschlüsselung]]
- [[Public-Key-Verschlüsselung]] mit [[Hash-Funktion]]
- Digitale Signatur mit Verschlüsselung

**Explizite Algorithmen:**

- [[RSA-Signatur]]
- [[ElGama-Signatur]]
- [[Digital Signature Algorithm]]

## Kapitel 10 - Methoden zur Berechnung diskreter Logarithmen

[[Silver-Pohlig-Hellman-Methode]]

[[Baby-Step-Giant-Step-Methode]]
[[Index-Calculus-Methode]]
