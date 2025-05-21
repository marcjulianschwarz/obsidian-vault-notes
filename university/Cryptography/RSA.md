---
uni-module: "KRY"
---

# RSA

## Schlüsselerzeugung

Wir wählen mit Hilfe eines [[Primzahltest]] verschieden [[Primzahl|Primzahlen]] $p_A,q_A$ und berechnen
$$N_A=p_Aq_A.$$
Dabei sollten $p_A$ und $q_A$ so gewählt werden (groß), sodass man die Primfaktorzerlegung von $N_A$ praktisch nicht berechnen kann.

Außerdem wählen wir eine Zahl $e_A>1$ mit
$$ggT(e_A, (p_A-1)(q_A-1))=1$$
und berechnen zum Beispiel mit Hilfe des [[Erweiterter Euklidischer Algorithmus|erweiterten euklidischen Algorithmus]] ein $d_A$ mit
$$e_Ad_A\equiv 1 \bmod (p_A-1)(q_A-1).$$
Also [[Modulo Invertierbarkeit|Inverses]] von $e_A$.

Der [[Address|Public Key]] ist das Tupel $(N_A, e_A)$, wobei $(N_A, d_A)$ der [[Private Key]] ist.

## Verschlüsselung

Wir besorgen uns einen öffentlichen Schlüssel $(N_A, e_A)$ und wandeln unseren [[Klartext]] in eine Zahlenfolge $a_1,\dots$ mit $a_i\leq N_A-1$ um.

Dann berechnen wir mit der [[Square-And-Multiply-Methode zum Potenzieren|Square-And-Multiply-Methode]] den Chiffretext mit
$$b_i=a_i^{e_A}\bmod N_A.$$

## Entschlüsselung

Wir erhalten eine Zahlenfolge $b_1,\dots$ und berechnen mit unserem privaten Schlüssel $(N_a, d_A)$ mit der [[Square-And-Multiply-Methode zum Potenzieren|Square-And-Multiply-Methode]] den [[Klartext]] mit
$$a_i=b_i^{d_A}\bmod N_A.$$

Die Zahlenfolge muss dann nur noch in Text umgewandelt werden.

## Anwendung

Das BSI empfiehlt eine Schlüssellänge $N_A$ von 3000 Bits.

Es ist bis heute kein Verfahren bekannt um
$$x^e \equiv b \bmod N$$
bei Kentniss von $N$ und $e$ für $b$ zu lösen, wenn man die Faktorisierung von $N$
nicht kennt.

Ansonsten kann man mit dem [[Euklidischer Algorithmus|euklidischen Algorithmus]] ein $d$ mit
$$e d \equiv 1 \bmod (p-1)(q-1)$$
berechnen ([[Modulo Invertierbarkeit]]). Dabei ist
$$b^d\bmod N$$
eine Lösung der Gleichung.
Auch den privaten Schlüssel kann man ohne Faktorisierung nicht berechnen.
