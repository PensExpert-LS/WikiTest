# GitHub Wiki Wissensdatenbank - Implementierungsanleitung

Diese Anleitung beschreibt, wie Sie die vorgefertigten Wiki-Seiten in Ihr GitHub Wiki übertragen.

## 📋 Voraussetzungen

- GitHub Account mit Schreibzugriff auf das Repository
- Git installiert auf Ihrem Computer
- Grundkenntnisse in Git-Befehlen

## 🚀 Schritt-für-Schritt Anleitung

### 1. GitHub Wiki aktivieren

1. Öffnen Sie Ihr GitHub Repository
2. Klicken Sie auf **Settings** (Einstellungen)
3. Scrollen Sie zum Abschnitt **Features**
4. Aktivieren Sie **Wikis** ✓

### 2. Wiki initialisieren

1. Klicken Sie auf den **Wiki**-Tab in Ihrem Repository
2. GitHub zeigt "Create the first page"
3. Sie können entweder:
   - Option A: Die erste Seite manuell erstellen (wird gleich überschrieben)
   - Option B: Direkt mit Git das Wiki-Repository klonen

### 3. Wiki-Repository klonen

Jedes GitHub Wiki hat ein eigenes Git-Repository. Die URL lautet:
```
https://github.com/[USERNAME]/[REPOSITORY].wiki.git
```

**Beispiel für dieses Template-Repository:**
```bash
# Wiki-Repository klonen
git clone https://github.com/PensExpert-LS/WikiTest.wiki.git

# In das Wiki-Verzeichnis wechseln
cd WikiTest.wiki
```

**Für Ihr eigenes Repository:**
```bash
# Ersetzen Sie [IhrOrg] und [IhrRepo] mit Ihren Werten
git clone https://github.com/[IhrOrg]/[IhrRepo].wiki.git

# In das Wiki-Verzeichnis wechseln
cd [IhrRepo].wiki
```

Falls das Wiki noch nicht existiert, erstellen Sie zunächst die erste Seite über die GitHub-Oberfläche, dann können Sie klonen.

### 4. Wiki-Seiten kopieren

#### Option A: Aus lokalem Repository kopieren

Wenn Sie das Haupt-Repository bereits geklont haben:

```bash
# Angenommen, beide Repositories sind nebeneinander
cp ../[IhrRepo]/wiki/*.md .

# Oder mit vollständigem Pfad
cp /pfad/zu/[IhrRepo]/wiki/*.md .
```

**Beispiel mit diesem Template:**
```bash
cp ../WikiTest/wiki/*.md .
```

#### Option B: Direkt von GitHub herunterladen

```bash
# Haupt-Repository klonen (falls noch nicht vorhanden)
git clone https://github.com/[IhrOrg]/[IhrRepo].git

# Wiki-Dateien kopieren
cp [IhrRepo]/wiki/*.md [IhrRepo].wiki/
```

**Beispiel mit diesem Template:**
```bash
git clone https://github.com/PensExpert-LS/WikiTest.git
cp WikiTest/wiki/*.md WikiTest.wiki/
```

### 5. Änderungen committen und pushen

```bash
# Zurück ins Wiki-Verzeichnis (passen Sie den Namen an)
cd [IhrRepo].wiki

# Status prüfen
git status

# Alle Dateien hinzufügen
git add .

# Commit erstellen
git commit -m "Initial wiki setup - Company knowledge base from template"

# Zum GitHub Wiki pushen
git push origin master
```

### 6. Wiki aufrufen und testen

1. Öffnen Sie: `https://github.com/[IhrOrg]/[IhrRepo]/wiki`
2. Sie sollten jetzt die Home-Seite sehen
3. Die Sidebar (Navigation) sollte links erscheinen
4. Der Footer sollte unten auf jeder Seite sichtbar sein

**Beispiel mit diesem Template:**
- URL: `https://github.com/PensExpert-LS/WikiTest/wiki`

## ✏️ Wiki-Seiten bearbeiten

### Im Browser

1. Navigieren Sie zu einer Wiki-Seite
2. Klicken Sie oben rechts auf **Edit**
3. Bearbeiten Sie den Markdown-Text
4. Fügen Sie eine beschreibende Commit-Message hinzu
5. Klicken Sie auf **Save Page**

### Lokal mit Git

```bash
# Wiki-Repository aktualisieren (passen Sie den Namen an)
cd [IhrRepo].wiki
git pull origin master

# Dateien bearbeiten
nano Home.md
# oder mit Ihrem bevorzugten Editor

# Änderungen committen
git add Home.md
git commit -m "Updated home page with company-specific information"
git push origin master
```

## 🎨 Anpassungen vornehmen

### Unternehmens-spezifische Informationen einfügen

1. **Kontaktdaten aktualisieren** (`Kontakt.md`)
   - E-Mail-Adressen ersetzen
   - Telefonnummern eintragen
   - Abteilungen anpassen

2. **Prozesse anpassen** (`Company-Processes.md`, `Urlaubsantrag.md`, etc.)
   - An Ihre Unternehmensrichtlinien anpassen
   - Spezifische Fristen eintragen
   - Tool-Namen aktualisieren

3. **Entwicklungsrichtlinien** (`Development-Guidelines.md`, `Git-Workflow.md`)
   - Coding Standards anpassen
   - Spezifische Tools/Frameworks ergänzen
   - Team-spezifische Workflows dokumentieren

### Neue Seiten hinzufügen

1. **Neue Markdown-Datei erstellen**
   ```bash
   cd [IhrRepo].wiki
   nano Neue-Seite.md
   ```

2. **In Sidebar verlinken** (`_Sidebar.md`)
   ```markdown
   ### Navigation
   ...
   - [Neue Seite](Neue-Seite)
   ```

3. **Von anderen Seiten verlinken**
   ```markdown
   Siehe auch: [Neue Seite](Neue-Seite)
   ```

4. **Committen und pushen**
   ```bash
   git add Neue-Seite.md _Sidebar.md
   git commit -m "Added new wiki page"
   git push origin master
   ```

### Seiten umbenennen

Im Browser:
1. Seite öffnen
2. Edit klicken
3. Titel ändern
4. Save Page

Oder lokal:
```bash
git mv Alte-Seite.md Neue-Seite.md
# Alle internen Links in anderen Dateien aktualisieren!
git commit -m "Renamed page"
git push origin master
```

## 📚 Wiki-Struktur verstehen

### Spezielle Dateien

- **`Home.md`** - Startseite (wird automatisch als Einstiegspunkt angezeigt)
- **`_Sidebar.md`** - Navigation, erscheint links auf allen Seiten
- **`_Footer.md`** - Footer, erscheint unten auf allen Seiten

### Verzeichnisstruktur

```
[IhrRepo].wiki/
├── Home.md                      # Startseite
├── _Sidebar.md                  # Navigation
├── _Footer.md                   # Footer
├── Getting-Started.md           # Einstieg
├── Onboarding.md               # HR: Onboarding
├── Urlaubsantrag.md            # HR: Urlaub
├── Zeiterfassung.md            # HR: Zeiterfassung
├── Development-Guidelines.md   # Dev: Richtlinien
├── Git-Workflow.md             # Dev: Git
├── Code-Review.md              # Dev: Reviews
├── Company-Processes.md        # Prozesse
├── FAQ.md                      # FAQ
├── Kontakt.md                  # Kontakte
├── Wiki-Setup.md               # Wiki-Anleitung
└── Editing-Guidelines.md       # Bearbeitungs-Richtlinien
```

## 🔍 Tipps & Best Practices

### Markdown-Links

```markdown
# Interne Wiki-Links (Dateiname ohne .md)
[Getting Started](Getting-Started)
[FAQ](FAQ)

# Mit Anker zu Abschnitt
[FAQ - Entwicklung](FAQ#entwicklung)

# Externe Links
[GitHub Docs](https://docs.github.com)
```

### Bilder einbinden

```markdown
# Externe Bilder
![Alt-Text](https://example.com/image.png)

# Bilder im Wiki hochladen:
# 1. Bearbeiten Sie eine Seite
# 2. Ziehen Sie das Bild in den Editor
# 3. GitHub lädt es automatisch hoch und fügt den Link ein
```

### Suchfunktion nutzen

- Suchfeld oben rechts im Wiki
- Durchsucht alle Seiten
- Unterstützt Volltextsuche

### Versionierung

- Jede Änderung wird als Git-Commit gespeichert
- Klicken Sie auf "Page History" um Änderungen zu sehen
- Frühere Versionen können wiederhergestellt werden

## ⚠️ Wichtige Hinweise

### Zugriffsrechte

- **Public Repository**: Wiki ist öffentlich sichtbar
- **Private Repository**: Nur für Repository-Mitglieder
- Schreibrechte wie beim Repository

### Synchronisation

```bash
# Vor Bearbeitung: Immer pullen
git pull origin master

# Nach Bearbeitung: Pushen
git push origin master
```

### Konflikte vermeiden

- Nicht gleichzeitig dieselbe Seite bearbeiten
- Regelmäßig pullen bei Team-Arbeit
- Bei Konflikten: Manuell in Datei auflösen

## 🆘 Problemlösung

### Wiki lässt sich nicht klonen

**Problem**: `Repository not found`

**Lösung**:
1. Stellen Sie sicher, dass das Wiki aktiviert ist
2. Erstellen Sie die erste Seite über die Web-Oberfläche
3. Versuchen Sie es erneut

### Sidebar wird nicht angezeigt

**Problem**: Navigation erscheint nicht

**Lösung**:
1. Dateiname muss exakt `_Sidebar.md` sein
2. Underscore nicht vergessen!
3. Nach Push aktualisieren Sie die Browser-Seite

### Links funktionieren nicht

**Problem**: Link führt zu 404

**Lösung**:
- Prüfen Sie den Dateinamen (ohne `.md`)
- Groß-/Kleinschreibung beachten
- Leerzeichen werden zu `-` (z.B. `Getting Started` → `Getting-Started`)

## 📞 Weitere Hilfe

- [GitHub Wiki Dokumentation](https://docs.github.com/en/communities/documenting-your-project-with-wikis)
- [Markdown Guide](https://guides.github.com/features/mastering-markdown/)
- [GitHub Community Forum](https://github.community/)

## ✅ Checkliste

Nach der Einrichtung:

- [ ] Wiki ist aktiviert
- [ ] Alle Seiten sind übertragen
- [ ] Home-Seite wird korrekt angezeigt
- [ ] Sidebar erscheint auf allen Seiten
- [ ] Footer ist sichtbar
- [ ] Interne Links funktionieren
- [ ] Unternehmens-spezifische Daten eingefügt
- [ ] Team ist informiert

## 🎉 Fertig!

Ihre Wissensdatenbank ist jetzt einsatzbereit. Viel Erfolg!

---

**Hinweis**: Dieses Template verwendet `PensExpert-LS/WikiTest` als Beispiel-Repository. Ersetzen Sie alle Repository-spezifischen Verweise durch Ihre eigenen Werte (Organisation/Repository-Name).

Bei Fragen: [Issue erstellen](https://github.com/PensExpert-LS/WikiTest/issues)
