# 🎯 ALTERNATIVE LÖSUNG - Ohne Gradle Installation

## Problem
Die PowerShell erkennt Chocolatey/Gradle nicht, weil sie vor der Installation geöffnet wurde.

## ✅ Einfachste Lösung: IntelliJ IDEA (5 Minuten Setup)

### Schritt 1: IntelliJ IDEA herunterladen
1. Gehe zu: https://www.jetbrains.com/idea/download/
2. Scrolle nach unten zu **"IntelliJ IDEA Community Edition"**
3. Klicke auf **"Download"** (kostenlos!)
4. Installiere die heruntergeladene `.exe` Datei

### Schritt 2: Projekt öffnen
1. Starte IntelliJ IDEA
2. Klicke auf **"Open"**
3. Navigiere zu: `C:\Users\v1358\Desktop\minecraft-damage-farm-mod`
4. Wähle den Ordner aus und klicke **"OK"**

### Schritt 3: Warten (wichtig!)
- IntelliJ erkennt automatisch, dass es ein Gradle-Projekt ist
- Unten rechts siehst du: "Gradle sync in progress..."
- **Warte 5-10 Minuten** - IntelliJ lädt alle Abhängigkeiten herunter
- Du siehst einen Fortschrittsbalken

### Schritt 4: Mod bauen
1. Rechts in IntelliJ: Klicke auf den **"Gradle"** Tab (Elefanten-Symbol)
2. Öffne: `minecraft-damage-farm-mod` → `Tasks` → `build`
3. **Doppelklick** auf `build`
4. Unten öffnet sich ein Fenster mit Build-Output
5. Warte bis "BUILD SUCCESSFUL" erscheint (5-10 Minuten beim ersten Mal)

### Schritt 5: JAR-Datei finden
1. Links im Projekt-Explorer: Öffne `build` → `libs`
2. Rechtsklick auf `damage-farm-mod-1.0.0.jar`
3. Wähle **"Show in Explorer"**

### Schritt 6: In Minecraft installieren
1. Drücke `Windows + R`
2. Tippe: `%APPDATA%\.minecraft\mods`
3. Drücke Enter
4. Kopiere `damage-farm-mod-1.0.0.jar` hierhin

---

## 🔄 Alternative 2: Visual Studio Code (wenn du VS Code bevorzugst)

### Schritt 1: Java Extension Pack installieren
1. Öffne VS Code
2. Gehe zu Extensions (Strg+Shift+X)
3. Suche: "Extension Pack for Java"
4. Installiere es

### Schritt 2: Projekt öffnen
1. File → Open Folder
2. Wähle: `C:\Users\v1358\Desktop\minecraft-damage-farm-mod`

### Schritt 3: Gradle Task ausführen
1. Drücke `Ctrl+Shift+P`
2. Tippe: "Gradle: Run Task"
3. Wähle: `build`
4. Warte auf "BUILD SUCCESSFUL"

---

## 🔄 Alternative 3: Gradle manuell installieren (ohne Chocolatey)

### Schritt 1: Gradle herunterladen
1. Gehe zu: https://gradle.org/releases/
2. Lade die neueste Version herunter (Binary-only)
3. Entpacke nach: `C:\Gradle`

### Schritt 2: PATH hinzufügen
1. Drücke `Windows + Pause`
2. Klicke "Erweiterte Systemeinstellungen"
3. Klicke "Umgebungsvariablen"
4. Unter "Systemvariablen" → Wähle "Path" → "Bearbeiten"
5. Klicke "Neu"
6. Füge hinzu: `C:\Gradle\gradle-8.x\bin`
7. Klicke überall "OK"

### Schritt 3: PowerShell NEU starten und bauen
```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
gradle wrapper
.\gradlew.bat build
```

---

## 🎯 Meine Empfehlung für dich

**IntelliJ IDEA Community Edition** ist die einfachste Lösung:
- ✅ Komplett kostenlos
- ✅ Alles automatisch
- ✅ Keine manuelle Konfiguration
- ✅ Funktioniert garantiert
- ✅ Professionelle IDE für zukünftige Mod-Entwicklung

**Download:** https://www.jetbrains.com/idea/download/

---

## ⏱️ Zeitaufwand mit IntelliJ

- Download & Installation: 5 Minuten
- Projekt öffnen: 1 Minute
- Erste Gradle Sync: 5-10 Minuten
- Build: 5-10 Minuten
- **Gesamt: ca. 20-30 Minuten**

Aber danach kannst du den Mod jederzeit in 1-2 Minuten neu bauen!

---

## 📞 Welche Methode möchtest du?

Sag mir einfach:
- **"IntelliJ"** → Ich führe dich durch IntelliJ IDEA
- **"VS Code"** → Ich führe dich durch VS Code
- **"Gradle manuell"** → Ich helfe dir bei der manuellen Installation