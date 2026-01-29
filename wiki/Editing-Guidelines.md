# Editing Guidelines

Richtlinien für das Bearbeiten und Erstellen von Wiki-Seiten.

## 🎯 Ziel

Diese Guidelines helfen dabei, konsistente und qualitativ hochwertige Wiki-Inhalte zu erstellen.

## ✍️ Allgemeine Grundsätze

### Klarheit vor Perfektion
- Lieber einfach und verständlich als perfekt
- Schreiben Sie für Ihr Publikum
- Vermeiden Sie Fachjargon wo möglich

### Aktualität
- Halten Sie Informationen aktuell
- Markieren Sie veraltete Inhalte
- Entfernen Sie obsolete Informationen

### Konsistenz
- Folgen Sie den Formatierungs-Standards
- Nutzen Sie einheitliche Terminologie
- Behalten Sie die Struktur bei

## 📐 Seitenstruktur

### Standard-Template

```markdown
# Seitentitel

Kurze Einleitung (1-2 Sätze was diese Seite behandelt)

## 🎯 Übersicht (optional)

Überblick über den Inhalt

## Hauptabschnitt 1

Inhalt...

## Hauptabschnitt 2

Inhalt...

## 📚 Weiterführende Links

- [Related Page 1](Link)
- [Related Page 2](Link)

---

[Zurück zur Startseite](Home)
```

### Überschriften

- `#` für Seitentitel (nur einmal pro Seite)
- `##` für Hauptabschnitte
- `###` für Unterabschnitte
- `####` und tiefer sparsam verwenden

## 🎨 Formatierung

### Hervorhebungen

```markdown
**Wichtig** - Fett für wichtige Begriffe
*Emphasis* - Kursiv für Betonung
`code` - Backticks für Code, Befehle, Dateinamen
```

### Listen

```markdown
Aufzählung:
- Punkt 1
- Punkt 2
  - Unterpunkt 2.1
  - Unterpunkt 2.2

Nummerierte Liste:
1. Schritt 1
2. Schritt 2
3. Schritt 3

Checkliste:
- [ ] Nicht erledigt
- [x] Erledigt
```

### Code-Blöcke

````markdown
Inline: `npm install`

Block:
```bash
npm install
npm start
```

Mit Syntax-Highlighting:
```javascript
function example() {
  return "hello";
}
```
````

### Zitate und Hinweise

```markdown
> 💡 **Tipp**: Nützlicher Hinweis

> ⚠️ **Achtung**: Wichtige Warnung

> ℹ️ **Info**: Zusätzliche Information
```

## 🔗 Links

### Interne Wiki-Links

```markdown
[Seitentitel](Seitenname)
[Getting Started](Getting-Started)
[FAQ](FAQ)
```

### Externe Links

```markdown
[GitHub Documentation](https://docs.github.com)
```

### Links zu Issues/PRs

```markdown
Siehe Issue #123
Implementiert in PR #456
```

### Anker-Links

```markdown
## Abschnitt 1 {#section-1}

Später: Siehe [Abschnitt 1](#section-1)
```

## 🖼️ Bilder und Medien

### Bilder einbinden

```markdown
![Beschreibender Alt-Text](https://url-zum-bild.png)
```

### Screenshots

- Speichern als PNG
- Beschreibende Dateinamen
- Hochladen in separates Assets-Repo oder Wiki
- Alt-Text für Barrierefreiheit

### Diagramme

```markdown
Nutzen Sie Tools wie:
- Mermaid für Diagramme
- Draw.io für komplexe Grafiken
- ASCII-Art für einfache Visualisierungen
```

## 📋 Tabellen

```markdown
| Spalte 1 | Spalte 2 | Spalte 3 |
|----------|----------|----------|
| Wert 1   | Wert 2   | Wert 3   |
| Wert 4   | Wert 5   | Wert 6   |

Ausrichtung:
| Links    | Zentriert | Rechts   |
|:---------|:---------:|---------:|
| Text     | Text      | Text     |
```

## 🎭 Emojis

Verwenden Sie Emojis sparsam und konsistent:

```markdown
📚 Dokumentation
🚀 Getting Started, Deployment
💡 Tipps
⚠️ Warnungen
✅ Erfolg, Checklisten
❌ Fehler, Verboten
🔧 Konfiguration, Tools
🎯 Ziele
📝 Notizen
🔗 Links
```

## ✅ Qualitätskriterien

### Vor dem Speichern prüfen

- [ ] Rechtschreibung und Grammatik
- [ ] Alle Links funktionieren
- [ ] Code-Beispiele sind korrekt
- [ ] Formatierung ist konsistent
- [ ] Informationen sind aktuell
- [ ] Sidebar-Links aktualisiert (falls neue Seite)

### Commit-Messages

```markdown
Gut:
- "Added API documentation"
- "Updated onboarding process"
- "Fixed broken links in FAQ"

Schlecht:
- "Update"
- "Changes"
- "WIP"
```

## 🏗️ Neue Seite erstellen

### Prozess

1. **Planung**
   - Zweck der Seite definieren
   - Zielgruppe identifizieren
   - Struktur skizzieren

2. **Erstellung**
   - Template verwenden
   - Inhalt schreiben
   - Formatieren

3. **Integration**
   - In Sidebar verlinken
   - Von relevanten Seiten verlinken
   - In Home-Seite aufnehmen (falls wichtig)

4. **Review**
   - Selbst durchlesen
   - Feedback einholen (optional)
   - Veröffentlichen

## 📝 Seitentypen

### Prozessdokumentation

```markdown
# Prozess-Titel

## 🎯 Ziel
Wofür ist dieser Prozess?

## 📋 Voraussetzungen
Was wird benötigt?

## 🔄 Schritt-für-Schritt
1. Schritt 1
2. Schritt 2

## ⚠️ Wichtige Hinweise
Besonderheiten

## 📞 Ansprechpartner
Wer hilft bei Fragen?
```

### Technische Dokumentation

```markdown
# Feature/Tool-Name

## 📖 Übersicht
Was ist das?

## 🚀 Quick Start
Schnelleinstieg

## 📚 Detaillierte Anleitung
Ausführliche Erklärung

## 🔧 Konfiguration
Setup-Details

## ❓ Troubleshooting
Häufige Probleme
```

### Richtlinien

```markdown
# Richtlinien-Titel

## 🎯 Zweck
Warum gibt es diese Richtlinien?

## 📋 Regeln
1. Regel 1
2. Regel 2

## ✅ Best Practices
Empfehlungen

## ❌ Zu vermeiden
Anti-Patterns
```

## 🔄 Bestehende Seiten aktualisieren

### Kleine Änderungen
- Tippfehler
- Veraltete Links
- Kleine Ergänzungen

→ Direkt bearbeiten und speichern

### Größere Änderungen
- Strukturänderungen
- Inhaltliche Überarbeitung
- Neue Abschnitte

→ Ggf. im Team besprechen

## 🗑️ Seiten löschen

Vor dem Löschen prüfen:
- [ ] Wird die Seite noch gebraucht?
- [ ] Gibt es Links von anderen Seiten?
- [ ] Sollte Inhalt archiviert werden?

Alternative: Seite als "veraltet" markieren.

## 🔍 Suchoptimierung

- **Aussagekräftige Titel**: Beschreiben Sie den Inhalt
- **Schlüsselwörter**: Wichtige Begriffe im ersten Absatz
- **Synonyme**: Verschiedene Begriffe für dasselbe Konzept
- **Querverweise**: Links zu verwandten Themen

## 📞 Hilfe und Feedback

Bei Fragen:
- Siehe [FAQ](FAQ)
- Fragen Sie im Team
- Kontaktieren Sie die Wiki-Maintainer

Feedback willkommen:
- Verbesserungsvorschläge
- Fehlerhinweise
- Neue Ideen

---

[Zurück zur Startseite](Home)
