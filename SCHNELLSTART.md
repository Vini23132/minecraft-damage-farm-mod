# 🚀 SCHNELLSTART - Einfachster Weg zur JAR-Datei

## Der absolut einfachste Weg: Chocolatey (5 Minuten)

### Schritt 1: PowerShell als Administrator öffnen
1. Drücke `Windows-Taste`
2. Tippe: `PowerShell`
3. **Rechtsklick** auf "Windows PowerShell"
4. Wähle: **"Als Administrator ausführen"**

### Schritt 2: Chocolatey installieren
Kopiere diesen **kompletten Befehl** und füge ihn in PowerShell ein:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Drücke `Enter` und warte ca. 30 Sekunden.

### Schritt 3: Java und Gradle installieren
Kopiere diesen Befehl:

```powershell
choco install openjdk21 gradle -y
```

Drücke `Enter` und warte ca. 2-3 Minuten (lädt und installiert automatisch).

### Schritt 4: PowerShell schließen und NEU öffnen (WICHTIG!)
- Schließe die Administrator-PowerShell
- Öffne eine **normale** PowerShell (nicht als Admin)

### Schritt 5: Zum Mod-Ordner navigieren
```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
```

### Schritt 6: Gradle Wrapper erstellen
```powershell
gradle wrapper
```

Warte ca. 10 Sekunden.

### Schritt 7: Mod bauen
```powershell
.\gradlew.bat build
```

**Beim ersten Mal dauert das 5-10 Minuten** (lädt viele Dateien herunter).
Du siehst viele Zeilen mit "Download..." - das ist normal!

### Schritt 8: Fertige JAR-Datei finden
Die fertige Datei ist hier:
```
C:\Users\v1358\Desktop\minecraft-damage-farm-mod\build\libs\damage-farm-mod-1.0.0.jar
```

Öffne den Ordner mit:
```powershell
explorer build\libs
```

### Schritt 9: In Minecraft installieren
1. Drücke `Windows + R`
2. Tippe: `%APPDATA%\.minecraft\mods`
3. Drücke `Enter`
4. Kopiere `damage-farm-mod-1.0.0.jar` in diesen Ordner

---

## ✅ Fertig!

Starte Minecraft mit Fabric Loader 1.21.11 und der Mod ist installiert!

---

## 🔄 Alternative: IntelliJ IDEA (wenn Chocolatey nicht funktioniert)

### Schritt 1: IntelliJ IDEA herunterladen
1. Gehe zu: https://www.jetbrains.com/idea/download/
2. Lade **Community Edition** herunter (kostenlos)
3. Installiere es

### Schritt 2: Projekt öffnen
1. Starte IntelliJ IDEA
2. Klicke auf "Open"
3. Wähle den Ordner: `C:\Users\v1358\Desktop\minecraft-damage-farm-mod`
4. Klicke "OK"

### Schritt 3: Warten
IntelliJ lädt automatisch alle Abhängigkeiten herunter (5-10 Minuten).

### Schritt 4: Bauen
1. Rechts in IntelliJ: Klicke auf "Gradle"
2. Öffne: `minecraft-damage-farm-mod` → `Tasks` → `build`
3. Doppelklick auf `build`

### Schritt 5: JAR-Datei finden
Die Datei ist in: `build/libs/damage-farm-mod-1.0.0.jar`

---

## 📋 Zusammenfassung - Kopiere diese Befehle nacheinander:

```powershell
# 1. PowerShell als Admin öffnen, dann:
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

# 2. Java und Gradle installieren:
choco install openjdk21 gradle -y

# 3. PowerShell schließen und NEU öffnen (normal, nicht Admin)

# 4. Zum Ordner navigieren:
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod

# 5. Wrapper erstellen:
gradle wrapper

# 6. Mod bauen:
.\gradlew.bat build

# 7. Ordner öffnen:
explorer build\libs

# 8. Mods-Ordner öffnen:
explorer %APPDATA%\.minecraft\mods

# 9. damage-farm-mod-1.0.0.jar von build\libs nach mods kopieren
```

**Das war's! 🎉**