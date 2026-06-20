# 🎯 SCHNELLSTART - Speziell für dich

## ✅ Chocolatey ist bereits installiert!

Du hast Chocolatey schon, also können wir direkt loslegen!

---

## Schritt 1: Java und Gradle installieren

Öffne PowerShell als **Administrator** und führe aus:

```powershell
choco install openjdk21 gradle -y
```

Warte ca. 2-3 Minuten bis die Installation fertig ist.

---

## Schritt 2: PowerShell schließen und NEU öffnen

**WICHTIG:** Schließe die PowerShell komplett und öffne eine **neue normale PowerShell** (nicht als Administrator).

---

## Schritt 3: Überprüfen ob alles installiert ist

```powershell
java -version
gradle -v
```

Du solltest sehen:
- Java: `openjdk version "21.x.x"`
- Gradle: `Gradle 8.x`

---

## Schritt 4: Zum Mod-Ordner navigieren

```powershell
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod
```

---

## Schritt 5: Gradle Wrapper erstellen

```powershell
gradle wrapper
```

Dauert ca. 10 Sekunden.

---

## Schritt 6: Mod bauen

```powershell
.\gradlew.bat build
```

**Beim ersten Mal dauert das 5-10 Minuten!**

Du siehst viele Zeilen wie:
- "Download https://..."
- "BUILD SUCCESSFUL"

Das ist normal und bedeutet, dass alles funktioniert!

---

## Schritt 7: Fertige JAR-Datei finden

```powershell
explorer build\libs
```

Die Datei **damage-farm-mod-1.0.0.jar** ist deine fertige Mod!

---

## Schritt 8: In Minecraft installieren

```powershell
explorer %APPDATA%\.minecraft\mods
```

Kopiere die **damage-farm-mod-1.0.0.jar** in diesen Ordner.

---

## 🎮 Fertig!

Starte Minecraft mit Fabric Loader 1.21.11 und drücke F8 zum Aktivieren!

---

## 📋 Alle Befehle auf einen Blick:

```powershell
# 1. PowerShell als Admin - Java & Gradle installieren:
choco install openjdk21 gradle -y

# 2. PowerShell schließen und NEU öffnen (normal)

# 3. Überprüfen:
java -version
gradle -v

# 4. Zum Ordner:
cd C:\Users\v1358\Desktop\minecraft-damage-farm-mod

# 5. Wrapper erstellen:
gradle wrapper

# 6. Mod bauen:
.\gradlew.bat build

# 7. Ordner öffnen:
explorer build\libs

# 8. Mods-Ordner öffnen:
explorer %APPDATA%\.minecraft\mods

# 9. JAR-Datei von build\libs nach mods kopieren
```

---

## ❓ Probleme?

### "gradle: command not found"
→ PowerShell neu starten (wichtig!)

### "JAVA_HOME not set"
→ PowerShell neu starten

### Build schlägt fehl
→ Führe aus: `.\gradlew.bat clean build`

### Dauert sehr lange
→ Normal beim ersten Mal! Gradle lädt viele Dateien herunter.

---

## ⏱️ Zeitplan:

- Java/Gradle Installation: 2-3 Minuten
- Erster Build: 5-10 Minuten
- Kopieren & Installieren: 1 Minute

**Gesamt: ca. 10-15 Minuten** 🚀