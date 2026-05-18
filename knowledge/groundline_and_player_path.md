# Groundline and Player Path

## Wichtigste Regel

Geometry Dash hat im Editor bereits einen eingebauten Boden. Dieser Ground ist die Standard-Laufbahn des Cube. Die KI soll keinen kuenstlichen Boden aus Blockobjekten bauen, nur weil ein Level Gameplay braucht.

## Was die KI bauen soll

Die KI baut Aufgaben auf den vorhandenen Ground:

- einzelne Spikes auf der Laufbahn
- kurze Plattformen als Variation
- kleine Waende oder Saeulen als Design
- klare Landepunkte nach Spruengen

Die KI baut nicht automatisch:

- eine durchgehende Reihe aus Blockobjekten bei Y `105`
- einen kompletten Boden aus Objekt-ID `1`
- Gameplay weit ueber dem Spieler, das man einfach unterlaufen kann

## Praktische Koordinaten

- Spieler startet links und laeuft nach rechts.
- Beginne sinnvolle Gameplay-Objekte ab X `180` bis `240`.
- Groundline: etwa Y `105`.
- Ground-Spike: exakt Y `105`.
- Nicht fuer Ground-Spikes verwenden: Y `120`, Y `150`, Y `200` oder hoeher.
- Kleine Plattform: nur wenn verlangt, etwa Y `120` bis Y `135`.
- Platform-Laenge fuer einfache Spruenge: 2 bis 4 Bloecke.
- X-Abstand zwischen einfachen Spikes: mindestens etwa `90` bis `150`.

## Warum zu hohe Objekte falsch sind

Wenn ein Spike oder Block weit ueber der Groundline liegt, muss der Spieler nicht springen. Der Cube laeuft unten weiter und das Objekt ist nur Deko oder ein Fehler. Gameplay-Hindernisse muessen dort liegen, wo die Spieler-Hitbox sie beruehrt, wenn nicht gesprungen wird.

## Gute Mini-Patterns

Einzelner Ground-Spike:

```text
LEVELSTRING:
1,8,2,270,3,105;
```

Zwei einfache Spruenge mit Abstand:

```text
LEVELSTRING:
1,8,2,270,3,105;1,8,2,450,3,105;
```

Ground-Spike plus kurze Plattform:

```text
LEVELSTRING:
1,8,2,270,3,105;1,1,2,420,3,120;1,1,2,450,3,120;1,8,2,570,3,105;
```

## Schlechte Mini-Patterns

Nicht als Standard erzeugen:

```text
LEVELSTRING:
1,1,2,150,3,105;1,1,2,180,3,105;1,1,2,210,3,105;1,1,2,240,3,105;1,1,2,270,3,105;
```

Grund: Das ist nur ein kuenstlicher Boden. Der echte GD-Boden ist schon da.

Nicht zu hoch platzieren:

```text
LEVELSTRING:
1,8,2,270,3,240;1,8,2,420,3,260;
```

Grund: Der Spieler laeuft darunter durch; es entsteht keine Sprungaufgabe.
