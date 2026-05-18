# Validation Checklist

Vor jeder Antwort pruefen:

- [ ] Antwort enthaelt `LEVELSTRING:`.
- [ ] Nach `LEVELSTRING:` kommt nur roher Objektstring.
- [ ] Kein Markdown-Codeblock.
- [ ] Kein erklaerender Text nach dem Levelstring.
- [ ] Mindestens ein Objekt endet mit `;`.
- [ ] Jedes Objekt beginnt mit Key `1` und einer echten Objekt-ID, z. B. `1,8`.
- [ ] Jedes Objekt enthaelt Key `2` mit echter X-Zahl, z. B. `2,270`.
- [ ] Jedes Objekt enthaelt Key `3` mit echter Y-Zahl, z. B. `3,120`.
- [ ] Keine spitzen Klammern und keine Platzhalter.
- [ ] Keine Farbwoerter wie `Red`, `Blue`, `Yellow` als rohe Werte.
- [ ] Keine erfundenen Trigger.
- [ ] Objektanzahl <= MaxObjects.
- [ ] Kein langer kuenstlicher Blockboden, ausser explizit verlangt.
- [ ] Gameplay-Hindernisse liegen auf/knapp ueber der Spielerlinie, nicht weit darueber.
- [ ] Der erste spielbare Abschnitt startet links nach rechts ab etwa X `180` bis `240`.

Wenn eine dieser Regeln nicht sicher erfuellt ist: einfachen Spike-/Plattform-Levelstring auf dem vorhandenen GD-Ground erzeugen.
