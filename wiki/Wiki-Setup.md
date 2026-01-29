# Wiki Setup Guide

Anleitung zur Einrichtung und Nutzung des GitHub Wiki für Ihre Wissensdatenbank.

## 🎯 Was ist GitHub Wiki?

GitHub Wiki ist ein integriertes Wiki-System für GitHub-Repositories, das sich perfekt für:
- Unternehmensdokumentation
- Wissensdatenbanken
- Projekt-Dokumentation
- Team-Richtlinien

eignet - ähnlich wie Confluence, aber direkt in GitHub integriert.

## 🚀 Wiki aktivieren

### Schritt 1: Wiki aktivieren

1. Gehen Sie zu Ihrem GitHub-Repository
2. Klicken Sie auf **Settings** (Einstellungen)
3. Scrollen Sie zu **Features**
4. Aktivieren Sie **Wikis**

### Schritt 2: Erste Seite erstellen

1. Klicken Sie auf den **Wiki** Tab
2. Klicken Sie auf **Create the first page**
3. Die Home-Seite wird automatisch erstellt

## 📂 Wiki-Struktur aus diesem Repository nutzen

Dieses Repository enthält vorgefertigte Wiki-Seiten im `/wiki`-Verzeichnis:

### Wiki-Inhalte übertragen

```bash
# 1. Wiki-Repository klonen
git clone https://github.com/IhrOrg/IhrRepo.wiki.git

# 2. Wiki-Seiten aus diesem Repository kopieren
cd IhrRepo.wiki
cp /pfad/zu/WikiTest/wiki/*.md .

# 3. Committen und pushen
git add .
git commit -m "Initial wiki setup from template"
git push origin master
```

### Enthaltene Seiten

- `Home.md` - Startseite
- `_Sidebar.md` - Seitenleiste (Navigation)
- `_Footer.md` - Fußzeile
- `Getting-Started.md` - Einstiegsanleitung
- `Onboarding.md` - Mitarbeiter-Onboarding
- `Development-Guidelines.md` - Entwicklungsrichtlinien
- `Git-Workflow.md` - Git-Arbeitsablauf
- `Code-Review.md` - Code-Review-Prozess
- `Company-Processes.md` - Unternehmensprozesse
- `FAQ.md` - Häufig gestellte Fragen

## ✏️ Wiki bearbeiten

### Im Browser

1. Navigieren Sie zur Wiki-Seite
2. Klicken Sie auf **Edit**
3. Bearbeiten Sie den Markdown-Text
4. Fügen Sie eine Commit-Message hinzu
5. Klicken Sie auf **Save Page**

### Lokal (Git)

```bash
# Wiki klonen
git clone https://github.com/IhrOrg/IhrRepo.wiki.git

# Bearbeiten
cd IhrRepo.wiki
# Dateien bearbeiten

# Committen und pushen
git add .
git commit -m "Updated documentation"
git push origin master
```

## 🎨 Spezielle Seiten

### Home.md
Die Startseite des Wiki. Wird automatisch angezeigt.

### _Sidebar.md
Erstellt eine Sidebar mit Navigation auf allen Seiten.

```markdown
### Navigation

**[🏠 Home](Home)**

---

**Bereich 1**
- [Seite 1](Seite-1)
- [Seite 2](Seite-2)
```

### _Footer.md
Erstellt einen Footer auf allen Seiten.

```markdown
---
📖 Wiki | [Issues](link) | [Kontakt](link)
```

## 📝 Markdown-Tipps für Wiki

### Links zu anderen Wiki-Seiten

```markdown
[Link Text](Seitenname)
[Getting Started](Getting-Started)
```

### Überschriften und Struktur

```markdown
# Hauptüberschrift
## Unterüberschrift
### Weitere Ebene

- Aufzählungspunkt
- Noch einer

1. Nummerierte Liste
2. Punkt 2
```

### Hervorhebungen

```markdown
**Fett** und *kursiv*

> Zitat oder wichtiger Hinweis

`Code inline`

\`\`\`javascript
// Codeblock
function example() {
  return true;
}
\`\`\`
```

### Tabellen

```markdown
| Spalte 1 | Spalte 2 | Spalte 3 |
|----------|----------|----------|
| Wert 1   | Wert 2   | Wert 3   |
| Wert 4   | Wert 5   | Wert 6   |
```

### Emojis

```markdown
:tada: :rocket: :book: :bulb: :warning:
```

Oder direkt: 🎉 🚀 📖 💡 ⚠️

### Bilder

```markdown
![Alt-Text](https://url-zum-bild.png)
```

## 🔐 Zugriffsrechte

- **Public Repository**: Wiki ist öffentlich
- **Private Repository**: Nur für Mitarbeiter mit Zugriff
- **Berechtigungen**: Gleiche wie für das Repository

## 🔍 Suche nutzen

GitHub Wiki hat eine integrierte Suchfunktion:
- Oben rechts im Wiki
- Durchsucht alle Seiten
- Unterstützt Volltextsuche

## 📊 Versionierung

Jede Wiki-Änderung wird als Git-Commit gespeichert:
- Volle Historie verfügbar
- **"Page History"** klicken für Verlauf
- Alte Versionen wiederherstellen möglich

## 🔄 Workflow-Integration

### Issues verlinken

```markdown
Siehe Issue #123 für Details
Fixes #456
```

### Pull Requests verlinken

```markdown
Implementiert in PR #789
```

### Code verlinken

```markdown
[Code](https://github.com/Org/Repo/blob/main/src/file.js#L10-L20)
```

## 🎓 Best Practices

### Struktur

- ✅ Klare Hierarchie
- ✅ Sinnvolle Kategorisierung
- ✅ Sidebar für Navigation
- ✅ Home-Seite als Übersicht

### Inhalt

- ✅ Kurz und prägnant
- ✅ Aktuelle Informationen
- ✅ Beispiele nutzen
- ✅ Screenshots bei UI-Themen

### Wartung

- ✅ Regelmäßig aktualisieren
- ✅ Veraltete Infos entfernen
- ✅ Feedback einarbeiten
- ✅ Team einbeziehen

## 🆚 Wiki vs. README vs. Docs

| Feature | Wiki | README | /docs |
|---------|------|--------|-------|
| Zweck | Wissensdatenbank | Projekt-Übersicht | Detaillierte Docs |
| Bearbeitung | Browser + Git | Nur Git | Nur Git |
| Struktur | Viele Seiten | Eine Datei | Viele Dateien |
| Versioned | Git (separat) | Git (mit Code) | Git (mit Code) |
| Ideal für | Prozesse, Guides | Quick Start | API Docs, Tutorials |

## 🔗 Weiterführende Links

- [GitHub Wiki Dokumentation](https://docs.github.com/en/communities/documenting-your-project-with-wikis)
- [Markdown Guide](https://guides.github.com/features/mastering-markdown/)
- [Getting Started](Getting-Started) in dieser Wiki

## 💡 Tipps

- **Template nutzen**: Verwenden Sie die Seiten aus diesem Repo als Basis
- **Regelmäßig updaten**: Wiki lebt von Aktualität
- **Team einbeziehen**: Jeder kann beitragen
- **Einfach starten**: Nicht perfekt sein müssen, lieber anfangen

---

[Zurück zur Startseite](Home)
