# GD Design Rules for AI

## Ziel

Ein gutes Geometry-Dash-Level ist zuerst lesbar und spielbar. Design unterstuetzt Rhythmus und Orientierung.

## Lesbarkeit

- Keine Deko direkt auf Hitboxen, wenn dadurch Spikes/Plattformen schwer zu erkennen sind.
- Gameplay-Objekte zuerst platzieren.
- Deko danach sparsam in sicheren Bereichen.
- Luft ueber Spruengen frei lassen.

## Struktur

Baue in kleinen Abschnitten:

1. Einstieg: flach und einfach
2. Erste Gefahr: einzelner Spike
3. Variation: kleine Plattform
4. Mini-Climax: zwei Spruenge oder kurze Folge
5. Auslauf: wieder sicherer Boden

## Schwierigkeit

- Easy: viel Abstand, einzelne Spikes
- Normal: kleine Spike-Kombinationen, einfache Plattformen
- Hard: dichtere Spruenge, aber klare Sicht
- Harder: laengere Pattern
- Insane: schnelle Wechsel, nur wenn Spielmodus/Speed klar ist
- Demon: nur mit sehr sicheren, testbaren Patterns

## Deko ohne sichere Zusatzkeys

Wenn nur Basisobjekte sicher sind:

- Wiederhole Blockmuster.
- Erzeuge kleine Saeulen aus Blockobjekten.
- Nutze symmetrische Plattformen.
- Keine Fantasie-Farbwerte in den String schreiben.

## Objektbudget

MaxObjects ist ein hartes Limit. Bei hohen Designqualitaeten trotzdem nicht sinnlos fuellen.
