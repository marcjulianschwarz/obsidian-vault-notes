---
uni-module: KonzMod

alias:
---

# DTD

Wird verwendet um ein Dokumen zu _validieren_. Es bieter Informationen über das Dokument und macht [[XML]] Dokumente untereinander vergleichbar.
Analog zum Schema einer [[Datenbank]].

```xml
<!DOCTYPE name [
	<!ELEMENT name Inhaltsmodell>
]>
```

## Inhaltsmodell

Enthält andere Elementtypen oder `#PCDATA`. Mit Operatoren können diese Elemente noch genauer beschrieben werden. Ein Plus steht für mindestens ein, ein Fragezeichen für Optional (ohne das Fragezeichen muss jedes Element vorkommen), ein Strich für Oder und ein Stern für beliebig.

## Attributtyp Definitionen

Zu jedem Element können auch noch Attribute wie folgt definiert werden:

```xml
<!ATTLIST Elementname
	Attributname Typ Attributbedingungen
>
```

Attributtypen können Zeichenketten (CDATA), IDs, Referenzen (IDREFS) oder NMTOKENS sein.
Attributbedingungen:

- `#REQUIRED`
- `#IMPLIED`
- `[#FIXED] "Vorbelegung"`
