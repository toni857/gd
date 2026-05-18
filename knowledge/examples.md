# Valid Examples

Diese Beispiele nutzen den eingebauten Geometry-Dash-Ground. Sie bauen keinen kuenstlichen Blockboden.

## 5 Sekunden, sehr einfach

```text
LEVELSTRING:
1,8,2,270,3,105;1,8,2,450,3,105;1,8,2,630,3,105;
```

## 5 Sekunden mit kleiner Plattform

```text
LEVELSTRING:
1,8,2,270,3,105;1,1,2,420,3,90;1,1,2,450,3,90;1,8,2,570,3,105;1,8,2,720,3,105;
```

## Sehr einfaches Spike-Pattern

```text
LEVELSTRING:
1,8,2,240,3,105;1,8,2,390,3,105;1,8,2,540,3,105;1,8,2,720,3,105;
```

## Kurze Plattform als Variation

```text
LEVELSTRING:
1,8,2,270,3,105;1,1,2,420,3,90;1,1,2,450,3,90;1,1,2,480,3,90;1,8,2,660,3,105;
```

## Falsch: Bodenlinie als Standard

```text
LEVELSTRING:
1,1,2,150,3,105;1,1,2,180,3,105;1,1,2,210,3,105;1,1,2,240,3,105;1,1,2,270,3,105;1,1,2,300,3,105;
```

Dieses Beispiel ist falsch, wenn der Nutzer nicht explizit Custom-Ground verlangt. GD hat bereits Ground.

## Falsch: zu hoch ueber der Spielerlinie

```text
LEVELSTRING:
1,8,2,300,3,240;1,8,2,480,3,260;
```

Dieses Beispiel ist falsch, weil der Spieler darunter durchlaeuft und nie springen muss.

## Falsch: kein GD-Objektstring

```text
LEVELSTRING:
6,1,10;8,20,-2,4,2,Red
```

Dieses Beispiel ist falsch und darf nicht erzeugt werden.
