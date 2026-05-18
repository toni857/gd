# Validation Checklist

Vor jeder Antwort pruefen:

- [ ] Antwort enthaelt `LEVELSTRING:`.
- [ ] Nach `LEVELSTRING:` kommt nur roher Objektstring.
- [ ] Kein Markdown-Codeblock.
- [ ] Kein erklaerender Text nach dem Levelstring.
- [ ] Mindestens ein Objekt endet mit `;`.
- [ ] Jedes Objekt beginnt mit `1,<Objekt-ID>`.
- [ ] Jedes Objekt enthaelt `2,<X>`.
- [ ] Jedes Objekt enthaelt `3,<Y>`.
- [ ] Keine Farbwoerter wie `Red`, `Blue`, `Yellow` als rohe Werte.
- [ ] Keine erfundenen Trigger.
- [ ] Objektanzahl <= MaxObjects.
- [ ] Kein langer kuenstlicher Blockboden, ausser explizit verlangt.
- [ ] Gameplay-Hindernisse liegen auf/knapp ueber der Spielerlinie, nicht weit darueber.
- [ ] Der erste spielbare Abschnitt startet links nach rechts ab etwa X `180` bis `240`.

Wenn eine dieser Regeln nicht sicher erfuellt ist: einfachen Spike-/Plattform-Levelstring auf dem vorhandenen GD-Ground erzeugen.
