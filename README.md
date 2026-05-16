# Geometry Dash Editor AI Knowledge

Diese Repository enthaelt die Regeln und Beispiele, die eine Editor-KI braucht, um in Geometry Dash nicht nur einen Plan zu schreiben, sondern direkt einfuegbare Level-Objekte zu liefern.

Wichtigster Einstieg:

- `knowledge/editor_ai_reference.md`
- `knowledge/levelstring_contract.md`
- `knowledge/examples.md`
- `knowledge/design_rules.md`
- `knowledge/validation_checklist.md`
- `levels/<level-id>.json`

Die Mod soll diese Daten als harte Vorgabe an die KI mitschicken. Wenn eine Antwort keinen echten `LEVELSTRING:` mit gueltigen GD-Objektstrings enthaelt, gilt sie als Fehler.

Der Ordner `levels/` ist fuer echte exportierte Suchergebnisse gedacht. Die Geode-Mod legt dort neue Dateien mit der Geometry-Dash-Level-ID als Dateinamen ab, zum Beispiel `levels/123456.json`.
