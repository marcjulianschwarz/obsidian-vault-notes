---
uni-module: "KRY"
---

# RSA-Signatur

## Schlüsselerzeugung

Jeder Teilnehmer besorgt sich einen [[RSA]] [[Address|Public Key]] und [[Private Key]] und einigt sich auf eine [[Hash-Funktion]] $H$.

## Signieren einer Nachricht

Bestimmung des Hashwert
$$h=H(M)$$
der Nachricht $M$.

Berechnung der RSA-Signatur
$$s=h^{d}\bmod N$$
mit dem [[Private Key]] $(N, d)$.

## Signaturüberprüfung

Bestimmung des Hashwert $h$, der Nachricht $M$.

Berechnung von
$$h^{\prime}=s^e \bmod N$$
mit dem [[Address|Public Key]] $(N,e)$ und Überprüfung
$$h^\prime=h\bmod N.$$

$$h^{\prime} \equiv s^{e_A} \equiv\left(h^{d_A}\right)^{e_A} \equiv h^{d_A e_A} \equiv h \bmod N_A$$
