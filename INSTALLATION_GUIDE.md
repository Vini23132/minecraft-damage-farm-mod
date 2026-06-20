# Vollständige Installations- und Nutzungsanleitung

## 📍 Wo befindet sich der Mod?

Der Mod befindet sich aktuell auf deinem Desktop:
```
C:\Users\v1358\Desktop\minecraft-damage-farm-mod
```

Dies ist der **Quellcode** des Mods. Um ihn in Minecraft zu nutzen, musst du ihn erst **kompilieren** (bauen).

---

## 🔧 Schritt 1: Voraussetzungen installieren

### 1.1 Java Development Kit (JDK) 21 installieren

1. Gehe zu: https://adoptium.net/de/temurin/releases/
2. Wähle:
   - **Version**: 21 (LTS)
   - **Betriebssystem**: Windows
   - **Architektur**: x64
3. Lade die `.msi` Datei herunter
4. Installiere sie mit Doppelklick
5. **Wichtig**: Aktiviere während der Installation die Option "Set JAVA_HOME variable"

**Überprüfung:**
```powershell
java -version
```
Sollte anzeigen: `openjdk version "21.x.x"`

### 1.2 Gradle installieren (Optional aber empfohlen)

**Option A - Mit Chocolatey (einfachste Methode):**
1. Öffne PowerShell als Administrator
2. Installiere Chocolatey (falls noch nicht vorhanden):
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
3. Installiere Gradle:
```powershell
choco install gradle
```

**Option B - Manuelle Installation:**
1. Gehe zu: https://gradle.org/releases/
2. Lade die neueste Version herunter (Binary-only)
3. Entpacke sie nach `C:\Gradle`
4. Füge `C:\Gradle\gradle-x.x\bin` zu deinem PATH hinzu

**Überprüfung:**
```powershell
gradle -v
```

---

## 🏗️ Schritt 2: Mod kompilieren (bauen)

### 2.1 Gradle Wrapper erstellen

Öffne PowerShell und navigiere zum Mod-Ordner:

```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
gradle wrapper
```

Dies erstellt die Dateien `gradlew.bat` und `gradlew`, die du zum Bauen brauchst.

### 2.2 Mod bauen

```powershell
.\gradlew.bat build
```

**Was passiert jetzt?**
- Gradle lädt alle benötigten Abhängigkeiten herunter (Minecraft, Fabric API, etc.)
- Der Java-Code wird kompiliert
- Eine `.jar` Datei wird erstellt

**Dauer:** Beim ersten Mal 5-10 Minuten (lädt viele Dateien herunter)

### 2.3 Fertige Mod-Datei finden

Nach erfolgreichem Build findest du die Mod-Datei hier:
```
C:\Users\v1358\Desktop\minecraft-damage-farm-mod\build\libs\damage-farm-mod-1.0.0.jar
```

---

## 🎮 Schritt 3: Minecraft mit Fabric vorbereiten

### 3.1 Fabric Loader installieren

1. Gehe zu: https://fabricmc.net/use/installer/
2. Lade den Fabric Installer herunter
3. Öffne die `.jar` Datei (Doppelklick)
4. Wähle:
   - **Minecraft Version**: 1.21.11
   - **Loader Version**: Neueste
   - **Installation Directory**: Standard (sollte automatisch erkannt werden)
5. Klicke auf "Install"

### 3.2 Fabric API installieren

1. Gehe zu: https://modrinth.com/mod/fabric-api/versions
2. Suche nach Version für **Minecraft 1.21.11**
3. Lade die `.jar` Datei herunter
4. Verschiebe sie in deinen Mods-Ordner:
```
%APPDATA%\.minecraft\mods\
```

**Mods-Ordner öffnen:**
- Drücke `Windows + R`
- Tippe: `%APPDATA%\.minecraft\mods`
- Drücke Enter
- Falls der Ordner nicht existiert, erstelle ihn

---

## 📦 Schritt 4: Mod installieren

1. Kopiere die Datei:
```
C:\Users\v1358\Desktop\minecraft-damage-farm-mod\build\libs\damage-farm-mod-1.0.0.jar
```

2. Füge sie ein in:
```
%APPDATA%\.minecraft\mods\
```

**Dein Mods-Ordner sollte jetzt enthalten:**
- `fabric-api-x.x.x+1.21.11.jar`
- `damage-farm-mod-1.0.0.jar`

---

## 🚀 Schritt 5: Minecraft starten und Mod nutzen

### 5.1 Minecraft starten

1. Öffne den Minecraft Launcher
2. Wähle das Profil **"fabric-loader-1.21.11"**
3. Klicke auf "Spielen"

### 5.2 Überprüfen, ob der Mod geladen wurde

1. Im Hauptmenü: Klicke auf "Mods"
2. Du solltest "Damage Farm Mod" in der Liste sehen

### 5.3 Farm aufbauen

**Benötigte Materialien:**
- 1x Magmablock
- 1x Sicherer Block (z.B. Stein, Erde, etc.)
- Nahrung in deiner Hotbar (z.B. Brot, Steak, etc.)

**Aufbau:**
```
[Sicherer Block] [Magmablock]
       ↑              ↑
    Hier heilen   Hier Schaden nehmen
```

1. Platziere einen Magmablock
2. Platziere direkt rechts daneben einen sicheren Block
3. Stelle dich auf den Magmablock
4. Stelle sicher, dass du Nahrung in deiner Hotbar (Slots 1-9) hast

### 5.4 Mod aktivieren

1. Drücke **F8** → Mod wird aktiviert
2. Du siehst im Chat: `[Damage Farm] Automation ENABLED`
3. Der Mod übernimmt jetzt die Steuerung

**Was passiert automatisch:**
- Du nimmst Schaden auf dem Magmablock
- Bei ≤2 Herzen: Bewegung zum sicheren Block
- Automatisches Essen von Nahrung
- Warten auf volle Gesundheit
- Rückkehr zum Magmablock
- Zyklus wiederholt sich

### 5.5 Mod deaktivieren

1. Drücke erneut **F8**
2. Du siehst im Chat: `[Damage Farm] Automation DISABLED`
3. Du hast wieder volle Kontrolle

---

## ⚙️ Einstellungen anpassen (Optional)

Wenn du die Schwellenwerte ändern möchtest, öffne diese Datei:
```
C:\Users\v1358\Desktop\minecraft-damage-farm-mod\src\main\java\com\damagefarm\DamageFarmAutomation.java
```

Ändere diese Werte (Zeilen 13-16):
```java
private static final float LOW_HEALTH_THRESHOLD = 4.0f;  // 2 Herzen (4.0 = 2 Herzen)
private static final float HIGH_HEALTH_THRESHOLD = 20.0f; // Volle Gesundheit
private static final int EATING_DURATION = 32;            // Ticks zum Essen
private static final int WAIT_AFTER_EATING = 20;          // Wartezeit nach Essen
```

Nach Änderungen:
1. Speichern
2. Mod neu bauen: `.\gradlew.bat build`
3. Neue `.jar` Datei in Mods-Ordner kopieren
4. Minecraft neu starten

---

## 🐛 Problemlösung

### "Gradle nicht gefunden"
- Installiere Gradle (siehe Schritt 1.2)
- Oder verwende IntelliJ IDEA / Eclipse zum Bauen

### "Java-Version nicht kompatibel"
- Stelle sicher, dass JDK 21 installiert ist
- Überprüfe mit: `java -version`

### "Mod lädt nicht in Minecraft"
- Überprüfe, ob Fabric Loader installiert ist
- Überprüfe, ob Fabric API im Mods-Ordner ist
- Überprüfe die Minecraft-Version (muss 1.21.11 sein)

### "Mod funktioniert nicht"
- Stelle sicher, dass du auf dem Magmablock stehst
- Stelle sicher, dass Nahrung in der Hotbar ist
- Drücke F8 zum Aktivieren
- Überprüfe die Chat-Nachrichten

### "Build schlägt fehl"
```powershell
.\gradlew.bat clean build
```

---

## 📝 Zusammenfassung der Befehle

```powershell
# Zum Mod-Ordner navigieren
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod

# Gradle Wrapper erstellen (einmalig)
gradle wrapper

# Mod bauen
.\gradlew.bat build

# Mods-Ordner öffnen
explorer %APPDATA%\.minecraft\mods

# Mod für Entwicklung testen (startet Minecraft direkt)
.\gradlew.bat runClient
```

---

## 🎯 Schnellstart-Checkliste

- [ ] JDK 21 installiert
- [ ] Gradle installiert
- [ ] Gradle Wrapper erstellt (`gradle wrapper`)
- [ ] Mod gebaut (`.\gradlew.bat build`)
- [ ] Fabric Loader installiert
- [ ] Fabric API im Mods-Ordner
- [ ] Damage Farm Mod im Mods-Ordner
- [ ] Farm aufgebaut (Magmablock + sicherer Block)
- [ ] Nahrung in Hotbar
- [ ] F8 drücken zum Aktivieren

Viel Erfolg mit deiner Survival-Challenge! 🎮