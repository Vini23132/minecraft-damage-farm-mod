# Build-Anleitung für den Damage Farm Mod

## Voraussetzungen

1. **Java Development Kit (JDK) 21** muss installiert sein
   - Download: https://adoptium.net/
   - Stelle sicher, dass `JAVA_HOME` korrekt gesetzt ist

2. **Gradle** (optional, da Gradle Wrapper verwendet werden kann)
   - Download: https://gradle.org/install/

## Build-Schritte

### Option 1: Mit Gradle Wrapper (empfohlen)

Wenn du Gradle installiert hast, erstelle zuerst den Wrapper:

```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
gradle wrapper
```

Dann baue den Mod:

```powershell
.\gradlew.bat build
```

### Option 2: Mit installiertem Gradle

```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
gradle build
```

### Option 3: Manueller Build in IntelliJ IDEA oder Eclipse

1. Öffne das Projekt in deiner IDE
2. Importiere es als Gradle-Projekt
3. Führe die Gradle-Task `build` aus
4. Die fertige JAR-Datei findest du in `build/libs/`

## Nach dem Build

Die fertige Mod-Datei findest du hier:
```
minecraft-damage-farm-mod/build/libs/damage-farm-mod-1.0.0.jar
```

Kopiere diese Datei in deinen Minecraft `mods`-Ordner:
```
%APPDATA%\.minecraft\mods\
```

## Troubleshooting

### "Gradle nicht gefunden"
- Installiere Gradle oder verwende eine IDE mit Gradle-Integration
- Alternativ: Lade den Gradle Wrapper manuell herunter

### "Java-Version nicht kompatibel"
- Stelle sicher, dass JDK 21 installiert ist
- Überprüfe mit: `java -version`

### Build-Fehler
- Lösche den `build`-Ordner und versuche es erneut
- Führe `gradle clean build` aus
- Stelle sicher, dass alle Abhängigkeiten heruntergeladen wurden

## Entwicklung

Für die Entwicklung kannst du den Mod direkt in Minecraft testen:

```powershell
.\gradlew.bat runClient
```

Dies startet Minecraft mit dem Mod bereits geladen.