# Code Review Prozess

Richtlinien für effektive Code Reviews im Team.

## 🎯 Ziel von Code Reviews

- **Qualitätssicherung**: Bugs früh erkennen
- **Wissensaustausch**: Vom Code anderer lernen
- **Konsistenz**: Einheitliche Code-Standards
- **Mentoring**: Entwickler unterstützen

## 📋 Checkliste für Reviewer

### Funktionalität
- [ ] Löst der Code das beschriebene Problem?
- [ ] Funktioniert der Code wie erwartet?
- [ ] Gibt es Edge Cases, die nicht behandelt werden?
- [ ] Sind alle Anforderungen erfüllt?

### Code-Qualität
- [ ] Ist der Code lesbar und verständlich?
- [ ] Folgt der Code unseren [Coding Standards](Development-Guidelines)?
- [ ] Sind Variablen und Funktionen gut benannt?
- [ ] Ist der Code ausreichend kommentiert?

### Testing
- [ ] Sind Tests vorhanden?
- [ ] Decken Tests die wichtigsten Szenarien ab?
- [ ] Laufen alle Tests erfolgreich?
- [ ] Sind Tests wartbar?

### Performance
- [ ] Gibt es offensichtliche Performance-Probleme?
- [ ] Werden Ressourcen effizient genutzt?
- [ ] Sind Datenbankabfragen optimiert?

### Security
- [ ] Gibt es potenzielle Sicherheitslücken?
- [ ] Wird Input validiert?
- [ ] Sind Zugriffsrechte korrekt implementiert?
- [ ] Werden Secrets korrekt behandelt?

### Dokumentation
- [ ] Ist die PR-Beschreibung aussagekräftig?
- [ ] Wurde relevante Dokumentation aktualisiert?
- [ ] Sind API-Änderungen dokumentiert?

## ✍️ Checkliste für Autoren

### Vor dem Review

- [ ] Code funktioniert lokal
- [ ] Alle Tests sind grün
- [ ] Code-Stil eingehalten (Linter)
- [ ] Keine Debug-Statements oder TODOs
- [ ] Commit-Messages sind aussagekräftig
- [ ] PR-Beschreibung ist vollständig

### PR-Beschreibung

Eine gute PR-Beschreibung enthält:

```markdown
## Änderungen
- Feature X implementiert
- Bug Y behoben

## Motivation
Warum sind diese Änderungen notwendig?

## Screenshots
(Bei UI-Änderungen)

## Testing
Wie wurde getestet?

## Checklist
- [ ] Tests hinzugefügt
- [ ] Dokumentation aktualisiert
- [ ] Breaking Changes dokumentiert
```

## 💬 Feedback geben

### Konstruktive Kommentare

✅ **Gut**:
```
Vorschlag: Diese Funktion könnte vereinfacht werden:
[Code-Beispiel]
Das würde die Lesbarkeit verbessern.
```

❌ **Nicht gut**:
```
Das ist falsch.
```

### Kategorien

Markieren Sie Ihre Kommentare:

- **🔴 Blocker**: Muss behoben werden
- **🟡 Suggestion**: Verbesserungsvorschlag
- **💡 Idea**: Überlegung für später
- **❓ Question**: Verständnisfrage
- **👍 Praise**: Positives Feedback

### Beispiele

```
🔴 Blocker: Diese Funktion hat einen Memory Leak.
Die Ressource wird nicht freigegeben.

🟡 Suggestion: Der Name `processData` könnte 
spezifischer sein, z.B. `validateUserInput`.

💡 Idea: In Zukunft könnten wir hier Caching 
einsetzen für bessere Performance.

❓ Question: Warum verwenden wir hier einen 
synchronen statt asynchronen Aufruf?

👍 Praise: Sehr elegant gelöst! Die Verwendung 
von Generatoren vereinfacht den Code erheblich.
```

## ⏱️ Zeitrahmen

- **Kleine PRs (<100 Zeilen)**: Innerhalb 1 Tag
- **Mittlere PRs (100-500 Zeilen)**: Innerhalb 2 Tage
- **Große PRs (>500 Zeilen)**: In kleinere aufteilen!

## 🔄 Review-Prozess

### 1. PR erstellen

```bash
# Branch pushen
git push origin feature/mein-feature

# PR auf GitHub erstellen
# Titel: feat(scope): Kurzbeschreibung
# Reviewer zuweisen
```

### 2. Automatische Checks

- CI/CD Pipeline läuft
- Tests werden ausgeführt
- Linter prüft Code-Stil
- Security Scans

### 3. Review

- Reviewer prüfen Code
- Feedback als Kommentare
- Diskussion bei Unklarheiten

### 4. Änderungen einarbeiten

```bash
# Feedback einarbeiten
git add .
git commit -m "fix: Review-Feedback eingearbeitet"
git push origin feature/mein-feature
```

### 5. Approval & Merge

- Mindestens 1 Approval
- Alle Checks grün
- Keine offenen Diskussionen
- Merge durchführen

## 🎨 Best Practices

### Für Autoren

1. **Klein halten**: Ideal sind 200-400 Zeilen
2. **Ein Thema**: Ein PR = Eine Aufgabe
3. **Tests**: Immer mit Tests
4. **Kontext**: Gute Beschreibung und Kommentare
5. **Responsive**: Zeitnah auf Feedback reagieren

### Für Reviewer

1. **Zeitnah**: Reviews priorisieren
2. **Konstruktiv**: Hilfreiche Kommentare
3. **Gründlich**: Nicht nur "LGTM"
4. **Code ausführen**: Bei Unsicherheit lokal testen
5. **Lernbereit**: Auch von PR-Autoren lernen

## 🚫 Anti-Patterns

❌ **Zu große PRs**: Schwer zu reviewen  
❌ **Spät reviewen**: Blockiert Entwicklung  
❌ **Nur "LGTM"**: Kein echter Review  
❌ **Persönliche Angriffe**: Unprofessionell  
❌ **Nitpicking**: Unwichtige Details  

## 📊 Metrics

Gute Indikatoren für Code Review Qualität:

- **Review Time**: Durchschnittlich < 1 Tag
- **PR Size**: Durchschnittlich < 400 Zeilen
- **Comments**: 2-5 Kommentare pro PR
- **Revisions**: 1-2 Runden

## 🛠️ Tools

- **GitHub**: PR-System, Kommentare
- **CI/CD**: Automatische Tests
- **Linters**: Code-Stil-Prüfung
- **SonarQube**: Code-Qualität (optional)

## 📚 Weiterführende Links

- [Development Guidelines](Development-Guidelines)
- [Git Workflow](Git-Workflow)
- [Testing Best Practices](Testing)

---

[Zurück zur Startseite](Home)
