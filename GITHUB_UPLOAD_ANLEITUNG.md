# 📤 GitHub Upload Anleitung - Schritt für Schritt

## Methode 1: GitHub Desktop (EINFACHSTE METHODE)

### Schritt 1: GitHub Desktop installieren
1. Gehe zu: https://desktop.github.com/
2. Klicke "Download for Windows"
3. Installiere die heruntergeladene Datei
4. Öffne GitHub Desktop

### Schritt 2: Bei GitHub anmelden
1. In GitHub Desktop: Klicke "Sign in to GitHub.com"
2. Melde dich mit deinem GitHub Account an (oder erstelle einen)

### Schritt 3: Repository erstellen
1. Klicke "File" → "New repository"
2. Name: `minecraft-damage-farm-mod`
3. Local path: Wähle `C:\Users\v1358\Desktop`
4. Klicke "Create repository"

### Schritt 4: Dateien hinzufügen
1. GitHub Desktop zeigt automatisch alle Dateien im Ordner
2. Unten links: Schreibe "Initial commit" als Summary
3. Klicke "Commit to main"

### Schritt 5: Auf GitHub hochladen
1. Klicke oben "Publish repository"
2. Entferne Haken bei "Keep this code private" (oder lasse ihn, wenn privat)
3. Klicke "Publish repository"

### Schritt 6: GitHub Actions aktivieren
1. Gehe zu deinem Repository auf GitHub.com
2. Klicke auf "Actions"
3. Klicke "I understand my workflows, go ahead and enable them"
4. Der Build startet automatisch!

### Schritt 7: JAR-Datei herunterladen
1. Warte 5-10 Minuten bis der Build fertig ist
2. Klicke auf den grünen Haken beim Build
3. Scrolle nach unten zu "Artifacts"
4. Klicke auf "damage-farm-mod" zum Download
5. Entpacke die ZIP-Datei
6. Die JAR-Datei ist drin!

---

## Methode 2: Direkt über GitHub Website (OHNE ZUSÄTZLICHE SOFTWARE)

### Schritt 1: Repository erstellen
1. Gehe zu: https://github.com/new
2. Repository name: `minecraft-damage-farm-mod`
3. Klicke "Create repository"

### Schritt 2: Dateien einzeln hochladen

**WICHTIG: Du musst die Ordnerstruktur beibehalten!**

#### 2.1 Hauptdateien hochladen:
1. Klicke "uploading an existing file"
2. Lade diese Dateien hoch:
   - `build.gradle`
   - `gradle.properties`
   - `settings.gradle`
   - `gradlew`
   - `gradlew.bat`
3. Klicke "Commit changes"

#### 2.2 src/main/java/com/damagefarm/ erstellen:
1. Klicke "Add file" → "Create new file"
2. Dateiname: `src/main/java/com/damagefarm/DamageFarmMod.java`
3. Kopiere den Inhalt aus deiner lokalen Datei
4. Klicke "Commit changes"
5. Wiederhole für `DamageFarmAutomation.java`

#### 2.3 src/main/resources/ erstellen:
1. Erstelle: `src/main/resources/fabric.mod.json`
2. Erstelle: `src/main/resources/assets/damagefarmmod/lang/en_us.json`
3. Erstelle: `src/main/resources/assets/damagefarmmod/lang/de_de.json`

#### 2.4 .github/workflows/ erstellen:
1. Erstelle: `.github/workflows/build.yml`
2. Kopiere den Inhalt aus deiner lokalen Datei

### Schritt 3: GitHub Actions aktivieren
1. Klicke auf "Actions"
2. Klicke "I understand my workflows, go ahead and enable them"
3. Der Build startet automatisch!

### Schritt 4: JAR-Datei herunterladen
1. Warte bis Build fertig ist (grüner Haken)
2. Klicke auf den Build
3. Scrolle zu "Artifacts"
4. Download "damage-farm-mod"

---

## Methode 3: Git Kommandozeile (FÜR FORTGESCHRITTENE)

### Voraussetzung: Git installieren
1. Gehe zu: https://git-scm.com/download/win
2. Installiere Git

### Befehle:
```powershell
# Zum Ordner navigieren
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod

# Git initialisieren
git init

# Alle Dateien hinzufügen
git add .

# Commit erstellen
git commit -m "Initial commit"

# Branch umbenennen
git branch -M main

# Remote hinzufügen (ersetze USERNAME mit deinem GitHub Username)
git remote add origin https://github.com/USERNAME/minecraft-damage-farm-mod.git

# Hochladen
git push -u origin main
```

---

## ⚡ SCHNELLSTE METHODE: GitHub Desktop

**Zeitaufwand: 5 Minuten**

1. GitHub Desktop installieren
2. Repository erstellen
3. "Publish repository" klicken
4. Fertig!

GitHub Actions baut dann automatisch die JAR-Datei.

---

## 📥 Nach dem Build

Die fertige JAR-Datei:
1. Herunterladen von GitHub Actions Artifacts
2. Entpacken (ist eine ZIP-Datei)
3. `damage-farm-mod-1.0.0.jar` in `%APPDATA%\.minecraft\mods\` kopieren

---

## ❓ Probleme?

### "Actions sind deaktiviert"
→ Gehe zu Settings → Actions → "Allow all actions"

### "Build schlägt fehl"
→ Überprüfe ob alle Dateien hochgeladen wurden
→ Besonders wichtig: `gradlew`, `gradlew.bat`, `.github/workflows/build.yml`

### "Kann Dateien nicht hochladen"
→ Nutze GitHub Desktop statt der Website

---

## 🎯 Empfehlung

**Nutze GitHub Desktop** - das ist mit Abstand am einfachsten:
- ✅ Keine Kommandozeile
- ✅ Keine einzelnen Dateien hochladen
- ✅ Alles automatisch
- ✅ 5 Minuten Setup

Download: https://desktop.github.com/