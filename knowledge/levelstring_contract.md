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
1,1,2,150,3,105;
```

Bedeutung:

- `1,1`: Objekt-ID 1
- `2,150`: X = 150
- `3,105`: Y = 105
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

```text
LEVELSTRING:
1,1,2,150,3,105;1,1,2,180,3,105;1,1,2,210,3,105;1,1,2,240,3,105;1,8,2,300,3,120;1,1,2,360,3,105;1,1,2,390,3,105;1,1,2,420,3,105;
```

## Laengenheuristik

Die KI soll fuer kurze Prompts nicht zu viele Objekte erzeugen:

- 5 Sekunden: 20 bis 80 Objekte
- 15 Sekunden: 80 bis 250 Objekte
- 30 Sekunden: 200 bis 600 Objekte
- MaxObjects ist immer hartes Limit

## Objektabstand

- Bodenbloecke: X in 30er-Schritten
- Spike-Abstand: mindestens 90 bis 150 X-Einheiten fuer einfache Schwierigkeit
- Plattformhoehen: Y `135`, `165`, `195` fuer einfache Variationen

## Keine erfundenen Trigger

Wenn Trigger-Keys nicht sicher sind, lasse sie weg. Ein einfaches spielbares Level ist besser als ein kaputter String.
