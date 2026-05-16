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

Wenn eine dieser Regeln nicht sicher erfuellt ist: einfachen Block/Spike-Levelstring erzeugen.
