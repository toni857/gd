# GD Design Rules for AI

## Ziel

Ein gutes Geometry-Dash-Level ist zuerst lesbar und spielbar. Design unterstuetzt Rhythmus und Orientierung.

## Ground zuerst verstehen

- Geometry Dash hat bereits eingebauten Ground.
- Die KI soll den vorhandenen Ground als Laufbahn benutzen.
- Keine langen Blockboeden bauen, ausser der Nutzer verlangt explizit Custom-Ground.
- Gameplay muss auf dem Spielerpfad liegen: Groundline Y `105`, Ground-Spikes exakt Y `105`.
- Nicht fuer Ground-Spikes verwenden: Y `120`, Y `150`, Y `200` oder hoeher.
- Block-ID `1` fuer niedrige Plattformen 30 Y-Einheiten tiefer setzen: meist Y `90`, nicht Y `120`.
- Objekte weit ueber der Laufbahn sind Deko, kein Hindernis.

## Lesbarkeit

- Gameplay-Objekte zuerst platzieren.
- Deko danach sparsam in sicheren Bereichen.
- Keine Deko direkt auf Hitboxen, wenn dadurch Spikes/Plattformen schwer zu erkennen sind.
- Luft ueber Spruengen frei lassen.
- Hindernisse nicht so hoch platzieren, dass der Spieler darunter durchlaeuft.

## Struktur

Baue in kleinen Abschnitten:

1. Einstieg: kurzer Vorlauf auf dem vorhandenen Ground
2. Erste Gefahr: einzelner Ground-Spike
3. Variation: kleine erreichbare Plattform oder zweiter Spike
4. Mini-Climax: zwei klare Spruenge oder kurze Folge
5. Auslauf: wieder vorhandenen Ground frei lassen

## Schwierigkeit

- Easy: viel Abstand, einzelne Spikes
- Normal: kleine Spike-Kombinationen, einfache Plattformen
- Hard: dichtere Spruenge, aber klare Sicht
- Harder: laengere Pattern
- Insane: schnelle Wechsel, nur wenn Spielmodus/Speed klar ist
- Demon: nur mit sehr sicheren, testbaren Patterns

## Deko ohne sichere Zusatzkeys

Wenn nur Basisobjekte sicher sind:

- Wiederhole kleine Blockmuster neben oder ueber dem Gameplay.
- Erzeuge kurze Saeulen aus Blockobjekten.
- Nutze symmetrische Plattformen.
- Nutze keine durchgehende Blockreihe als Boden.
- Keine Fantasie-Farbwerte in den String schreiben.

## Objektbudget

MaxObjects ist ein hartes Limit. Bei hohen Designqualitaeten trotzdem nicht sinnlos fuellen.
