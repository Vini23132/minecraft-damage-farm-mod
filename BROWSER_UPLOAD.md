# 🌐 GitHub Upload NUR im Browser - OHNE Apps!

## ✅ Ja, das geht komplett im Browser!

Du brauchst **KEINE** zusätzlichen Apps. Alles funktioniert direkt auf GitHub.com!

---

## 📝 Schritt-für-Schritt Anleitung

### Schritt 1: GitHub Account erstellen (falls noch nicht vorhanden)
1. Gehe zu: https://github.com/signup
2. Gib deine E-Mail-Adresse ein
3. Erstelle ein Passwort
4. Wähle einen Benutzernamen
5. Bestätige deine E-Mail-Adresse

### Schritt 2: Neues Repository erstellen
1. Gehe zu: https://github.com/new
2. **Repository name**: `minecraft-damage-farm-mod`
3. **Description** (optional): "Minecraft damage farm automation mod"
4. Wähle **Public** (damit GitHub Actions kostenlos ist)
5. Klicke **"Create repository"**

### Schritt 3: Dateien hochladen

#### 3.1 Erste Datei hochladen
1. Du siehst jetzt eine leere Repository-Seite
2. Klicke auf **"uploading an existing file"** (blauer Link)
3. Klicke **"choose your files"**
4. Navigiere zu: `C:\Users\v1358\Desktop\minecraft-damage-farm-mod`
5. Wähle **ALLE** Dateien aus (Strg+A)
6. Klicke "Öffnen"

**WICHTIG:** GitHub behält die Ordnerstruktur bei, wenn du alle Dateien auf einmal hochlädst!

#### 3.2 Commit erstellen
1. Unten auf der Seite siehst du "Commit changes"
2. Lass "Add files via upload" stehen
3. Klicke **"Commit changes"** (grüner Button)

### Schritt 4: Überprüfen
1. Du solltest jetzt alle Ordner und Dateien sehen:
   - `.github/`
   - `src/`
   - `build.gradle`
   - `gradle.properties`
   - `gradlew`
   - `gradlew.bat`
   - etc.

### Schritt 5: GitHub Actions aktivieren
1. Klicke oben auf **"Actions"**
2. Du siehst eine Warnung: "Workflows aren't being run on this repository"
3. Klicke **"I understand my workflows, go ahead and enable them"**
4. Der Build startet automatisch!

### Schritt 6: Build beobachten
1. Du siehst jetzt einen laufenden Workflow: "Build Minecraft Mod"
2. Klicke darauf
3. Du siehst den Fortschritt (gelber Kreis = läuft, grüner Haken = fertig)
4. **Warte 5-10 Minuten** beim ersten Mal

### Schritt 7: JAR-Datei herunterladen
1. Wenn der Build fertig ist (grüner Haken ✓)
2. Scrolle nach unten zu **"Artifacts"**
3. Klicke auf **"damage-farm-mod"**
4. Eine ZIP-Datei wird heruntergeladen

### Schritt 8: JAR-Datei extrahieren
1. Öffne die heruntergeladene ZIP-Datei
2. Darin ist die Datei: `damage-farm-mod-1.0.0.jar`
3. Extrahiere sie

### Schritt 9: In Minecraft installieren
1. Drücke `Windows + R`
2. Tippe: `%APPDATA%\.minecraft\mods`
3. Drücke Enter
4. Kopiere `damage-farm-mod-1.0.0.jar` in diesen Ordner

---

## 🎯 Zusammenfassung - Nur 9 Schritte!

```
1. GitHub Account erstellen
2. Repository erstellen
3. Alle Dateien hochladen (Strg+A)
4. Commit changes klicken
5. Actions aktivieren
6. 5-10 Minuten warten
7. Artifacts herunterladen
8. ZIP entpacken
9. JAR in Mods-Ordner kopieren
```

**Keine Apps nötig! Alles im Browser!** 🌐

---

## ❓ Häufige Fragen

### "Kann ich wirklich alle Dateien auf einmal hochladen?"
✅ Ja! Wähle einfach alle Dateien im Ordner aus (Strg+A) und lade sie hoch. GitHub behält die Ordnerstruktur bei.

### "Muss ich jeden Ordner einzeln erstellen?"
❌ Nein! Wenn du alle Dateien auf einmal hochlädst, erstellt GitHub die Ordner automatisch.

### "Wie lange dauert der Build?"
⏱️ Beim ersten Mal: 5-10 Minuten
⏱️ Danach: 2-5 Minuten

### "Ist GitHub Actions kostenlos?"
✅ Ja, für öffentliche Repositories komplett kostenlos!

### "Was ist, wenn der Build fehlschlägt?"
1. Überprüfe ob alle Dateien hochgeladen wurden
2. Besonders wichtig: `.github/workflows/build.yml`
3. Klicke auf den fehlgeschlagenen Build für Details

---

## 🔄 Dateien aktualisieren

Wenn du später Änderungen machen möchtest:

1. Gehe zu deinem Repository
2. Navigiere zur Datei, die du ändern möchtest
3. Klicke auf das Stift-Symbol (Edit)
4. Mache deine Änderungen
5. Klicke "Commit changes"
6. GitHub Actions baut automatisch neu!

---

## 📦 Alternative: ZIP hochladen

Falls das Hochladen aller Dateien nicht funktioniert:

1. Rechtsklick auf den Ordner `minecraft-damage-farm-mod`
2. "Senden an" → "ZIP-komprimierter Ordner"
3. Auf GitHub: Klicke "Add file" → "Upload files"
4. Ziehe die ZIP-Datei in den Browser
5. **WICHTIG:** Entpacke die ZIP auf GitHub nicht - lade die einzelnen Dateien hoch

---

## ✅ Vorteile der Browser-Methode

- ✅ Keine zusätzliche Software
- ✅ Funktioniert auf jedem Computer
- ✅ Automatischer Build
- ✅ Kostenlos
- ✅ Einfach zu bedienen

**Das ist die einfachste Methode ohne Apps!** 🎉