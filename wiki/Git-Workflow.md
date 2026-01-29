# Git Workflow

Unser standardisierter Git-Workflow für die Zusammenarbeit im Team.

## 🌳 Branch-Strategie

Wir verwenden einen modifizierten Git Flow:

### Main Branches

#### `main`
- Produktionsreifer Code
- Immer deploybar
- Geschützt (keine direkten Commits)
- Nur via Pull Requests

#### `develop`
- Integrationsbranch für Features
- Basis für neue Feature-Branches
- Regelmäßige Merges von Features

### Supporting Branches

#### `feature/*`
Format: `feature/beschreibung` oder `feature/TICKET-123-beschreibung`

```bash
# Feature-Branch erstellen
git checkout develop
git pull origin develop
git checkout -b feature/neue-login-seite

# Entwickeln und committen
git add .
git commit -m "feat(auth): Login-Seite hinzugefügt"

# Push und Pull Request
git push origin feature/neue-login-seite
# Dann PR auf GitHub erstellen
```

#### `bugfix/*`
Format: `bugfix/beschreibung`

```bash
git checkout develop
git checkout -b bugfix/login-fehler-beheben
```

#### `hotfix/*`
Format: `hotfix/beschreibung`

```bash
# Für dringende Produktions-Fixes
git checkout main
git checkout -b hotfix/kritischer-sicherheitsfehler
```

## 📝 Commit-Messages

### Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: Neues Feature
- `fix`: Bugfix
- `docs`: Dokumentation
- `style`: Formatierung
- `refactor`: Code-Umstrukturierung
- `test`: Tests hinzufügen/ändern
- `chore`: Build-Prozess, Tools

### Beispiele

```bash
# Gute Commits
git commit -m "feat(user): Benutzerregistrierung implementiert"
git commit -m "fix(api): Null-Pointer-Exception in getUserData behoben"
git commit -m "docs(readme): Installationsanleitung aktualisiert"

# Schlechte Commits
git commit -m "änderungen"
git commit -m "fix"
git commit -m "WIP"
```

### Mehrzeilige Commits

```bash
git commit -m "feat(payment): Stripe-Integration

- Stripe SDK integriert
- Zahlungsformular erstellt
- Webhook-Handler implementiert

Closes #123"
```

## 🔄 Pull Request Workflow

### 1. Vorbereitung

```bash
# Aktualisieren Sie develop
git checkout develop
git pull origin develop

# Rebase Ihres Feature-Branches
git checkout feature/mein-feature
git rebase develop

# Konflikte auflösen falls nötig
```

### 2. Pull Request erstellen

- Aussagekräftiger Titel
- Beschreibung der Änderungen
- Screenshots bei UI-Änderungen
- Referenz zu Issues/Tickets

### 3. Code Review

Siehe [Code Review Prozess](Code-Review)

- Mindestens 1 Approval erforderlich
- Alle Checks müssen grün sein
- Keine offenen Diskussionen

### 4. Merge

- **Squash and Merge** für Features
- **Merge Commit** für wichtige Releases
- Branch nach Merge löschen

## 🛠️ Nützliche Befehle

### Status und Übersicht

```bash
# Status anzeigen
git status

# Änderungen anzeigen
git diff

# Commit-Historie
git log --oneline --graph

# Branches anzeigen
git branch -a
```

### Arbeit mit Branches

```bash
# Branch wechseln
git checkout branch-name

# Neuen Branch erstellen und wechseln
git checkout -b new-branch

# Branch löschen
git branch -d branch-name

# Remote-Branch löschen
git push origin --delete branch-name
```

### Änderungen rückgängig machen

```bash
# Datei aus Staging entfernen
git reset HEAD datei.txt

# Lokale Änderungen verwerfen
git checkout -- datei.txt

# Letzten Commit rückgängig (lokal)
git reset --soft HEAD~1
```

### Sync mit Remote

```bash
# Alle Änderungen holen
git fetch --all

# Pull mit Rebase
git pull --rebase origin develop

# Force-Push (nur für Feature-Branches!)
git push --force-with-lease
```

## ⚠️ Wichtige Regeln

1. ✅ **Niemals direkt auf `main` oder `develop` pushen**
2. ✅ **Regelmäßig mit `develop` synchronisieren**
3. ✅ **Aussagekräftige Commit-Messages**
4. ✅ **Kleine, fokussierte Commits**
5. ✅ **Vor Push: Tests laufen lassen**
6. ❌ **Keine `--force` auf shared branches**
7. ❌ **Keine Merge-Commits auf Feature-Branches**
8. ❌ **Keine großen Binary-Dateien committen**

## 🆘 Häufige Probleme

### Merge-Konflikt

```bash
# 1. Konflikt anzeigen
git status

# 2. Dateien bearbeiten
# Konflikt-Marker entfernen (<<<<, ====, >>>>)

# 3. Als gelöst markieren
git add konflikt-datei.txt

# 4. Rebase fortsetzen
git rebase --continue
```

### Falscher Branch

```bash
# Änderungen zu anderem Branch verschieben
git stash
git checkout richtiger-branch
git stash pop
```

### Commit rückgängig machen

```bash
# Letzten Commit ändern
git commit --amend

# Commit rückgängig (mit neuem Commit)
git revert commit-hash
```

## 📚 Weiterführende Links

- [Git Documentation](https://git-scm.com/doc)
- [Development Guidelines](Development-Guidelines)
- [Code Review](Code-Review)

---

[Zurück zur Startseite](Home)
