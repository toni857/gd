# LEVELSTRING Contract

## Zweck

Die Mod erwartet einen Geometry-Dash-Levelstring, der direkt in den Editor eingefuegt werden kann. Ein Text, Plan, JSON, Pseudocode oder Kommentar ist kein Ergebnis.

## Pflichtformat

```text
LEVELSTRING:
1,<OBJECT_ID>,2,<X>,3,<Y>;1,<OBJECT_ID>,2,<X>,3,<Y>;
```

## Objekt-Grundstruktur

Ein Objekt:

```text
1,8,2,270,3,120;
```

Bedeutung:

- `1,8`: Objekt-ID 8, hier ein Spike
- `2,270`: X = 270
- `3,120`: Y = 120
- `;`: Ende des Objekts

## Falsch

```text
6,1,10;8,20,-2,4,2,Red
```

Warum falsch:

- Kein `1,<Objekt-ID>` am Objektanfang
- keine stabilen `2,<X>` und `3,<Y>` Positionen
- Farbwoerter wie `Red` sind kein sicherer roher GD-Key-Value-Wert

## Sicherer Minimal-Level

Der sichere Minimal-Level benutzt den vorhandenen GD-Ground und setzt nur Hindernisse/Plattformen:

```text
LEVELSTRING:
1,8,2,270,3,120;1,8,2,420,3,120;1,1,2,540,3,150;1,1,2,570,3,150;1,8,2,720,3,120;
```

## Ground-Regel

- Keine langen Blockboeden als Standard.
- Keine durchgehende Reihe `1,1,2,<X>,3,105;...`, ausser der Nutzer verlangt explizit Custom-Ground.
- Der GD-Ground ist bereits vorhanden.
- Hindernisse gehoeren auf die Spielerlinie, nicht weit darueber.

## Laengenheuristik

Die KI soll fuer kurze Prompts nicht zu viele Objekte erzeugen:

- 5 Sekunden: 5 bis 40 Objekte
- 15 Sekunden: 40 bis 160 Objekte
- 30 Sekunden: 120 bis 450 Objekte
- MaxObjects ist immer hartes Limit

## Objektabstand

- Erster sinnvoller Gameplay-X-Wert: etwa `180` bis `240`
- Ground-Spike: oft Y `120`
- Spike-Abstand: mindestens 90 bis 150 X-Einheiten fuer einfache Schwierigkeit
- Plattformhoehen: Y `135`, `150`, `165` fuer einfache Variationen
- Plattformen: 2 bis 4 Blockobjekte, nicht endlos weiterziehen

## Keine erfundenen Trigger

Wenn Trigger-Keys nicht sicher sind, lasse sie weg. Ein einfaches spielbares Level ist besser als ein kaputter String.
