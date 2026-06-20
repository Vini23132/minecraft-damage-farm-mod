# 🔧 GitHub Actions - Was du siehst und was zu tun ist

## Wenn du auf "Actions" klickst, siehst du verschiedene Möglichkeiten:

---

## Szenario 1: "Workflows aren't being run on this repository"

### Was du siehst:
```
Workflows aren't being run on this repository
Actions are disabled on this repository
```

### Was zu tun ist:
1. Du siehst einen grünen Button: **"I understand my workflows, go ahead and enable them"**
2. **Klicke auf diesen Button**
3. Die Seite lädt neu
4. Jetzt sollte automatisch ein Build starten!

---

## Szenario 2: Du siehst eine Liste mit Workflows

### Was du siehst:
- Eine Liste mit "Build Minecraft Mod" oder ähnlich
- Eventuell mit einem gelben Kreis (läuft gerade) oder grünem Haken (fertig)

### Was zu tun ist:
1. **Klicke auf den Workflow-Namen** (z.B. "Build Minecraft Mod")
2. Du siehst jetzt Details zum Build
3. Warte bis der Build fertig ist (grüner Haken ✓)
4. Scrolle nach unten zu **"Artifacts"**
5. Klicke auf **"damage-farm-mod"** zum Download

---

## Szenario 3: "There are no workflow runs yet"

### Was du siehst:
```
There are no workflow runs yet
Get started with GitHub Actions
```

### Was das bedeutet:
Die Workflow-Datei wurde noch nicht erkannt oder ist nicht korrekt hochgeladen.

### Was zu tun ist:
1. Gehe zurück zum **"Code"** Tab
2. Überprüfe ob der Ordner `.github/workflows/` existiert
3. Überprüfe ob die Datei `build.yml` darin ist
4. Falls nicht:
   - Klicke "Add file" → "Create new file"
   - Dateiname: `.github/workflows/build.yml`
   - Kopiere den Inhalt aus deiner lokalen Datei
   - Klicke "Commit changes"
5. Gehe zurück zu "Actions" - jetzt sollte ein Build starten!

---

## Szenario 4: Build läuft gerade

### Was du siehst:
- Ein gelber Kreis 🟡 neben dem Workflow-Namen
- "In progress" oder "Running"

### Was zu tun ist:
1. **Warten!** Der erste Build dauert 5-10 Minuten
2. Du kannst auf den Workflow klicken um Details zu sehen
3. Du siehst verschiedene Schritte:
   - ✓ Checkout code
   - ✓ Set up JDK 21
   - 🟡 Build with Gradle (dauert am längsten)
   - ⏳ Upload artifact
4. Wenn alles grün ist (✓), scrolle nach unten zu "Artifacts"

---

## Szenario 5: Build ist fertig

### Was du siehst:
- Ein grüner Haken ✓ neben dem Workflow
- "Success" oder "Completed"

### Was zu tun ist:
1. **Klicke auf den Workflow** (falls noch nicht geöffnet)
2. **Scrolle ganz nach unten**
3. Du siehst eine Sektion **"Artifacts"**
4. Darunter steht: **"damage-farm-mod"** mit einem Download-Symbol
5. **Klicke darauf** - eine ZIP-Datei wird heruntergeladen
6. **Entpacke die ZIP-Datei**
7. Darin ist: `damage-farm-mod-1.0.0.jar`
8. **Kopiere diese JAR-Datei** nach `%APPDATA%\.minecraft\mods`

---

## Szenario 6: Build ist fehlgeschlagen

### Was du siehst:
- Ein rotes X ❌ neben dem Workflow
- "Failed" oder "Error"

### Was zu tun ist:
1. **Klicke auf den fehlgeschlagenen Workflow**
2. Klicke auf den roten Schritt um Details zu sehen
3. Häufige Fehler:
   - **"gradlew: Permission denied"**: Die gradlew-Datei wurde nicht richtig hochgeladen
   - **"Could not find build.gradle"**: Dateien fehlen
   - **"Java version mismatch"**: Sollte nicht passieren, da wir JDK 21 verwenden

### Lösung:
1. Überprüfe ob ALLE Dateien hochgeladen wurden:
   - `build.gradle`
   - `gradle.properties`
   - `settings.gradle`
   - `gradlew`
   - `gradlew.bat`
   - `.github/workflows/build.yml`
   - Alle Dateien in `src/`
2. Falls Dateien fehlen, lade sie nach
3. Der Build startet automatisch neu

---

## 📸 Visueller Guide

### Schritt 1: Actions Tab
```
[Code] [Issues] [Pull requests] [Actions] [Projects] [Wiki] [Security]
                                    ↑
                              Hier klicken
```

### Schritt 2: Workflows aktivieren (falls nötig)
```
┌─────────────────────────────────────────────────────┐
│ Workflows aren't being run on this repository      │
│                                                     │
│ [I understand my workflows, go ahead and enable them] │
│                    ↑                                │
│              Hier klicken                           │
└─────────────────────────────────────────────────────┘
```

### Schritt 3: Workflow auswählen
```
All workflows
├─ 🟡 Build Minecraft Mod (in progress)  ← Klicken
├─ ✓ Build Minecraft Mod (success)      ← Oder hier
└─ ❌ Build Minecraft Mod (failed)
```

### Schritt 4: Artifacts herunterladen
```
┌─────────────────────────────────────┐
│ Build Minecraft Mod                 │
│ ✓ All checks have passed            │
│                                     │
│ ... (Build-Details) ...            │
│                                     │
│ Artifacts                           │
│ ├─ 📦 damage-farm-mod              │
│    └─ [Download] ← Hier klicken    │
└─────────────────────────────────────┘
```

---

## ❓ Häufige Fragen

### "Ich sehe keine Artifacts"
→ Der Build ist noch nicht fertig oder fehlgeschlagen
→ Warte bis der grüne Haken erscheint

### "Der Build dauert ewig"
→ Normal! Beim ersten Mal 5-10 Minuten
→ Gradle lädt viele Abhängigkeiten herunter

### "Ich sehe nur 'Get started with GitHub Actions'"
→ Die Workflow-Datei fehlt
→ Erstelle `.github/workflows/build.yml` manuell

### "Der Build schlägt immer fehl"
→ Überprüfe ob alle Dateien hochgeladen wurden
→ Besonders wichtig: `gradlew`, `gradlew.bat`, `build.gradle`

---

## 🎯 Zusammenfassung

1. **Actions Tab** öffnen
2. **"Enable workflows"** klicken (falls nötig)
3. **Warten** bis Build fertig ist (grüner Haken)
4. **Auf Workflow klicken**
5. **Nach unten scrollen** zu "Artifacts"
6. **"damage-farm-mod" herunterladen**
7. **ZIP entpacken**
8. **JAR-Datei in Mods-Ordner kopieren**

Fertig! 🎉