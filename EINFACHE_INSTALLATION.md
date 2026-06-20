# 🚀 Einfachste Installation - Ohne Kompilieren

Da du den Mod nicht selbst kompilieren möchtest, gibt es mehrere einfache Alternativen:

## Option 1: Online Build-Service nutzen (EMPFOHLEN)

### GitHub Actions (Kostenlos & Automatisch)

1. **GitHub Account erstellen** (falls noch nicht vorhanden):
   - Gehe zu: https://github.com/signup

2. **Repository erstellen**:
   - Klicke auf "New Repository"
   - Name: `minecraft-damage-farm-mod`
   - Klicke "Create repository"

3. **Code hochladen**:
   - Öffne PowerShell im Mod-Ordner:
   ```powershell
   cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/DEIN-USERNAME/minecraft-damage-farm-mod.git
   git push -u origin main
   ```

4. **GitHub Actions einrichten**:
   - Ich erstelle dir gleich eine Workflow-Datei
   - GitHub baut den Mod automatisch
   - Du kannst die fertige `.jar` Datei herunterladen

## Option 2: Modrinth/CurseForge Build-Service

1. Gehe zu: https://modrinth.com/
2. Erstelle einen Account
3. Lade den Quellcode hoch
4. Der Service baut den Mod automatisch

## Option 3: Online Java Compiler

1. Gehe zu: https://www.jdoodle.com/online-java-compiler/
2. Lade die Java-Dateien hoch
3. Kompiliere online

## Option 4: Lokale Installation mit Chocolatey (5 Minuten)

Das ist die **schnellste lokale Methode**:

### Schritt 1: PowerShell als Administrator öffnen
- Rechtsklick auf Windows-Start
- "Windows PowerShell (Administrator)" wählen

### Schritt 2: Chocolatey installieren
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

### Schritt 3: JDK und Gradle installieren
```powershell
choco install openjdk21 -y
choco install gradle -y
```

### Schritt 4: PowerShell neu starten und Mod bauen
```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
gradle wrapper
.\gradlew.bat build
```

### Schritt 5: Fertige Datei finden
```
C:\Users\v1358\Desktop\minecraft-damage-farm-mod\build\libs\damage-farm-mod-1.0.0.jar
```

---

## Option 5: Ich erstelle dir eine GitHub Action (AUTOMATISCH)

Wenn du mir erlaubst, erstelle ich eine GitHub Actions Workflow-Datei. Dann:

1. Du lädst den Code auf GitHub hoch
2. GitHub baut den Mod automatisch
3. Du lädst die fertige `.jar` Datei herunter

**Vorteil**: Komplett automatisch, keine lokale Installation nötig!

---

## 🎯 Meine Empfehlung

**Für dich am einfachsten: Option 4 (Chocolatey)**

Warum?
- ✅ Dauert nur 5 Minuten
- ✅ Alles automatisch
- ✅ Funktioniert garantiert
- ✅ Du kannst den Mod später selbst anpassen

**Befehle in Kurzform:**
```powershell
# 1. PowerShell als Admin öffnen
# 2. Chocolatey installieren (Befehl von oben)
# 3. Tools installieren:
choco install openjdk21 gradle -y

# 4. Neue PowerShell öffnen (normal, nicht Admin)
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
gradle wrapper
.\gradlew.bat build

# 5. Fertig! Datei ist in: build\libs\damage-farm-mod-1.0.0.jar
```

---

## ❓ Was möchtest du tun?

Sag mir einfach:
- "Option 1" → Ich erstelle GitHub Actions Workflow
- "Option 4" → Ich führe dich durch Chocolatey-Installation
- "Andere Idee" → Ich helfe dir weiter

Die fertige `.jar` Datei kannst du dann einfach in deinen Minecraft Mods-Ordner kopieren!