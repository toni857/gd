# Exported Geometry Dash Levels

Dieser Ordner wird von der Geode-Mod befuellt.

Dateiformat:

- Dateiname: `<level-id>.json`
- `level_string`: roher GD-Levelstring
- `object_count_from_levelstring`: Objektanzahl aus dem Levelstring
- `ai_usage`: kurzer Hinweis, wie die Editor-KI das Level als Stil- und Gameplay-Referenz verwenden soll

Diese Dateien sind Lern- und Referenzdaten. Die KI soll daraus Muster fuer Gameplay, Abstaende und Design ableiten, aber beim Generieren trotzdem einen neuen validen `LEVELSTRING:` ausgeben.
