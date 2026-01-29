# WikiTest - GitHub Wiki Wissensdatenbank

Test-Repository für GitHub Wiki Funktionalität als Unternehmens-Wissensdatenbank (ähnlich Confluence).

## 🎯 Zweck

Dieses Repository demonstriert, wie GitHub Wiki als Wissensdatenbank für Unternehmen genutzt werden kann. Es enthält:

- ✅ Vorgefertigte Wiki-Seitenstruktur
- ✅ Beispiel-Inhalte für typische Unternehmensdokumentation
- ✅ Navigation (Sidebar) und Footer
- ✅ Verschiedene Kategorien (Onboarding, Entwicklung, Prozesse, FAQ)

## 📚 Wiki-Struktur

Das Repository enthält im `/wiki` Verzeichnis fertige Wiki-Seiten:

### Hauptseiten
- `Home.md` - Startseite mit Übersicht
- `Getting-Started.md` - Einstiegsanleitung
- `FAQ.md` - Häufig gestellte Fragen

### Onboarding & HR
- `Onboarding.md` - Mitarbeiter-Onboarding
- `Urlaubsantrag.md` - Urlaubsprozess
- `Zeiterfassung.md` - Arbeitszeiterfassung

### Entwicklung
- `Development-Guidelines.md` - Coding Standards
- `Git-Workflow.md` - Git-Arbeitsablauf
- `Code-Review.md` - Review-Prozess

### Organisation
- `Company-Processes.md` - Unternehmensprozesse
- `Kontakt.md` - Ansprechpartner

### Wiki-Verwaltung
- `Wiki-Setup.md` - Anleitung zur Wiki-Einrichtung
- `Editing-Guidelines.md` - Richtlinien zum Bearbeiten

### Navigation
- `_Sidebar.md` - Seitenleiste für Navigation
- `_Footer.md` - Fußzeile auf allen Seiten

## 🚀 Wiki aktivieren und einrichten

### Schritt 1: Wiki aktivieren

1. Gehen Sie zu **Settings** → **Features**
2. Aktivieren Sie **Wikis**
3. Gehen Sie zum **Wiki**-Tab

### Schritt 2: Wiki-Inhalte übertragen

```bash
# Wiki-Repository klonen
git clone https://github.com/PensExpert-LS/WikiTest.wiki.git

# In Wiki-Verzeichnis wechseln
cd WikiTest.wiki

# Wiki-Seiten aus diesem Repository kopieren
cp ../wiki/*.md .

# Committen und pushen
git add .
git commit -m "Initial wiki setup with company knowledge base template"
git push origin master
```

### Schritt 3: Wiki nutzen

Navigieren Sie zu `https://github.com/PensExpert-LS/WikiTest/wiki` um das Wiki zu sehen!

## 🎨 Anpassungen

Die Wiki-Seiten sind als Template gedacht und können angepasst werden:

- Ersetzen Sie Beispiel-E-Mails und Telefonnummern
- Passen Sie Prozesse an Ihre Organisation an
- Fügen Sie weitere Seiten hinzu
- Löschen Sie nicht benötigte Abschnitte

## 📖 Weitere Informationen

- [GitHub Wiki Dokumentation](https://docs.github.com/en/communities/documenting-your-project-with-wikis)
- [Markdown Guide](https://guides.github.com/features/mastering-markdown/)
- Siehe `wiki/Wiki-Setup.md` für detaillierte Anleitung

## 💡 Vorteile von GitHub Wiki

- ✅ **Versionskontrolle** - Alle Änderungen werden getrackt
- ✅ **Markdown** - Einfache Formatierung
- ✅ **Zusammenarbeit** - Jeder kann beitragen
- ✅ **Suchfunktion** - Schnelles Finden
- ✅ **Integration** - Direkt mit Code-Repository verbunden
- ✅ **Kostenlos** - Für public und private Repositories

## 🔗 Links

- **Wiki**: [https://github.com/PensExpert-LS/WikiTest/wiki](https://github.com/PensExpert-LS/WikiTest/wiki)
- **Issues**: [Problem melden](https://github.com/PensExpert-LS/WikiTest/issues)

---

Viel Erfolg mit Ihrer Wissensdatenbank! 🎉
