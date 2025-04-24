---
uni-module: "IDB"

alias: ["buffer frames", "Kacheln"]
---

# Pufferrahmen

Ist eine Verallgemeinerung des [[Dateipuffer]].

Beim Lesen: Prefetching
Beim Schreiben: mehrere Blöcke füllen und dann schreiben

Besser als [[Wechselpuffertechnik]], da der [[Zugriffskamm]] Bewegungen spart.

**ABER:** Persistenz ist ein Problem → Der Puffer ist flüchtig, also wenn der Rechner ausfällt ist der gepufferte Speicher weg.
