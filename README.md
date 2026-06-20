# Damage Farm Mod für Minecraft 1.21.1 (Fabric)

Ein Minecraft-Mod, der den Schadensfarm-Prozess für Survival-Challenges automatisiert.

## Funktionen

- **F8-Taste**: Aktiviert/Deaktiviert die Automatisierung
- **Automatischer Zyklus**:
  1. Nimmt Schaden auf dem Magmablock
  2. Bewegt sich bei niedrigen HP (≤2 Herzen) zum sicheren Block
  3. Isst automatisch Nahrung aus der Hotbar
  4. Wartet auf vollständige Regeneration
  5. Kehrt zum Magmablock zurück
  6. Wiederholt den Zyklus

## Installation

1. Stelle sicher, dass du Fabric Loader für Minecraft 1.21.1 installiert hast
2. Lade Fabric API herunter und platziere sie im `mods`-Ordner
3. Baue den Mod mit: `./gradlew build` (Windows: `gradlew.bat build`)
4. Die fertige JAR-Datei findest du in `build/libs/`
5. Kopiere die JAR-Datei in deinen Minecraft `mods`-Ordner

## Verwendung

### Setup der Farm
1. Baue eine Farm mit einem Magmablock
2. Platziere einen sicheren Block direkt rechts neben dem Magmablock
3. Stelle dich auf den Magmablock
4. Stelle sicher, dass du Nahrung in deiner Hotbar hast

### Aktivierung
1. Drücke **F8**, um die Automatisierung zu aktivieren
2. Der Mod übernimmt die Steuerung und führt den Schadenszyklus aus
3. Drücke **F8** erneut, um die Automatisierung zu deaktivieren

## Konfiguration

Die folgenden Werte können in `DamageFarmAutomation.java` angepasst werden:

- `LOW_HEALTH_THRESHOLD`: Gesundheitsschwelle zum Verlassen des Magmablocks (Standard: 4.0 = 2 Herzen)
- `HIGH_HEALTH_THRESHOLD`: Gesundheitsschwelle zur Rückkehr (Standard: 20.0 = volle Gesundheit)
- `EATING_DURATION`: Dauer des Essens in Ticks (Standard: 32)
- `WAIT_AFTER_EATING`: Wartezeit nach dem Essen in Ticks (Standard: 20)

## Wichtige Hinweise

- Der Mod verwendet **keine Cheats** - alle Aktionen erfolgen durch normale Survival-Mechaniken
- Stelle sicher, dass du genügend Nahrung in deiner Hotbar hast
- Der Mod sucht automatisch nach Nahrung in den Hotbar-Slots (0-8)
- Die Bewegung erfolgt durch Seitwärtsbewegung (Strafe rechts/links)

## Technische Details

- **Minecraft Version**: 1.21.1
- **Mod Loader**: Fabric
- **Fabric API**: Erforderlich
- **Java Version**: 21

## Lizenz

MIT License