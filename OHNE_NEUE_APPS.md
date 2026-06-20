# 🎯 Lösung OHNE neue Apps - Nur PowerShell

## Problem
Die PowerShell hat die Umgebungsvariablen noch nicht aktualisiert.

## ✅ Lösung: PowerShell komplett neu starten

### Schritt 1: Alle PowerShell-Fenster schließen
- Schließe **ALLE** offenen PowerShell-Fenster
- Auch die Administrator-PowerShell
- Warte 5 Sekunden

### Schritt 2: Neue PowerShell als Administrator öffnen
1. Drücke `Windows-Taste`
2. Tippe: `PowerShell`
3. **Rechtsklick** auf "Windows PowerShell"
4. Wähle: **"Als Administrator ausführen"**

### Schritt 3: Java und Gradle installieren
```powershell
choco install openjdk21 gradle -y
```

Warte bis die Installation fertig ist (2-3 Minuten).

### Schritt 4: Überprüfen ob installiert
```powershell
refreshenv
java -version
gradle -v
```

Wenn du Versionen siehst → Perfekt!
Wenn nicht → Gehe zu Schritt 5

### Schritt 5: Umgebungsvariablen manuell aktualisieren
```powershell
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")
```

Dann nochmal testen:
```powershell
java -version
gradle -v
```

### Schritt 6: Zum Mod-Ordner navigieren
```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
```

### Schritt 7: Gradle Wrapper erstellen
```powershell
gradle wrapper
```

### Schritt 8: Mod bauen
```powershell
.\gradlew.bat build
```

Warte 5-10 Minuten beim ersten Mal.

### Schritt 9: JAR-Datei öffnen
```powershell
explorer build\libs
```

---

## 🔄 Alternative: Wenn Chocolatey nicht funktioniert

### Option A: Gradle manuell herunterladen (OHNE Installation)

1. **Gradle herunterladen:**
   - Gehe zu: https://gradle.org/releases/
   - Klicke auf "binary-only" bei der neuesten Version
   - Speichere die `.zip` Datei

2. **Entpacken:**
   - Rechtsklick auf die `.zip` → "Alle extrahieren"
   - Entpacke nach: `C:\Gradle`

3. **PowerShell öffnen und direkt verwenden:**
```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
C:\Gradle\gradle-8.10.2\bin\gradle.bat wrapper
.\gradlew.bat build
```

### Option B: Java JDK manuell herunterladen

1. **JDK herunterladen:**
   - Gehe zu: https://adoptium.net/de/temurin/releases/
   - Wähle: Version 21, Windows, x64
   - Lade `.msi` herunter und installiere

2. **Dann Gradle wie in Option A**

---

## 📋 Komplette Befehlsliste (kopiere alles auf einmal)

```powershell
# PowerShell als Admin öffnen, dann:

# 1. Installieren
choco install openjdk21 gradle -y

# 2. Umgebung aktualisieren
refreshenv

# 3. Testen
java -version
gradle -v

# 4. Falls nicht erkannt, manuell aktualisieren:
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")

# 5. Nochmal testen
java -version
gradle -v

# 6. Zum Ordner
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod

# 7. Wrapper erstellen
gradle wrapper

# 8. Bauen
.\gradlew.bat build

# 9. Ordner öffnen
explorer build\libs
```

---

## ❓ Wenn immer noch "gradle nicht gefunden"

Dann ist Chocolatey in der Admin-PowerShell nicht richtig installiert.

**Schnellste Lösung ohne neue Apps:**

1. **Gradle direkt herunterladen:**
   - https://gradle.org/releases/
   - "binary-only" → Speichern

2. **Entpacken nach C:\Gradle**

3. **Direkt verwenden:**
```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
C:\Gradle\gradle-8.10.2\bin\gradle.bat wrapper
.\gradlew.bat build
```

**Das funktioniert GARANTIERT ohne neue Apps!** 🎯