# Git und Versionskontrolle – Kursübersicht

Dieser Kurs vermittelt die Grundlagen der Versionskontrolle mit Git und die Verwaltung von Softwareprojektdateien. Er ist als zweitägiger Kurs konzipiert und folgt einer didaktischen Struktur von einfach zu komplex.

## Kursstruktur

### Tag 1: Grundlagen der Versionskontrolle

**Vormittag (09:00 - 12:30)**
- **Kapitel 3.1**: Historische Entwicklung und Bedarf an Versionskontrolle
- **Kapitel 3.2**: Grundlegende Konzepte und Terminologie
- **Kapitel 3.3**: Installation und erste Schritte mit Git

**Nachmittag (13:30 - 17:00)**
- **Kapitel 4.1**: Remote-Repositories und Collaboration
- **Kapitel 4.2**: GitHub/GitLab Integration
- **Kapitel 4.3**: Projektdateien und .gitignore Konfiguration

### Tag 2: Fortgeschrittene Git-Verwaltung und Projektstruktur

**Vormittag (09:00 - 12:30)**
- **Kapitel 5.1**: Fortgeschrittene Git-Features (Rebase, Stash, Cherry-Pick)
- **Kapitel 5.2**: Projektadministration und Best Practices

**Nachmittag (13:30 - 17:00)**
- Abschlussprojekt und praktische Anwendungen
- Zertifikatsvergabe

## Erstellte Inhalte

### Hauptseiten (9 Kapitel)
1. **content/2.md**: Kursübersicht und Lernziele
2. **content/3.md**: Historische Entwicklung der Versionskontrolle
3. **content/4.md**: Grundlegende Git-Konzepte (3 Zustände, Objekte, Referenzen)
4. **content/5.md**: Installation und erste Schritte mit Git
5. **content/6.md**: Remote-Repositories und Collaboration-Workflows
6. **content/7.md**: GitHub vs. GitLab Integration
7. **content/8.md**: Projektdateien und .gitignore Konfiguration
8. **content/9.md**: Fortgeschrittene Features (Rebase, Stash, Cherry-Pick, etc.)
9. **content/10.md**: Projektadministration und Best Practices

### Aufgaben (9 Aufgaben)
1. **tasks/02_00_01.yaml**: Kursverständnis
2. **tasks/03_00_01.yaml**: Historische Entwicklung verstehen
3. **tasks/04_00_01.yaml**: Git-Konzepte verstehen
4. **tasks/05_00_01.yaml**: Installation und erste Schritte
5. **tasks/06_00_01.yaml**: Remote-Repositories und Collaboration
6. **tasks/07_00_01.yaml**: GitHub/GitLab Integration
7. **tasks/08_00_01.yaml**: Projektdateien und .gitignore
8. **tasks/09_00_01.yaml**: Fortgeschrittene Git-Features
9. **tasks/10_00_01.yaml**: Projektadministration und Best Practices

### Navigation
- Aktualisierte **mkdocs.yml** mit neuer Navigation
- Aktualisierte **index.md** mit allen Kurskapiteln

## Didaktischer Ansatz

### Lernpfad von einfach zu komplex
1. **Historischer Kontext**: Warum ist Versionskontrolle notwendig?
2. **Grundkonzepte**: Was sind die fundamentalen Ideen?
3. **Praktische Anwendung**: Wie funktioniert es konkret?
4. **Teamarbeit**: Wie arbeitet man zusammen?
5. **Fortgeschrittene Features**: Wie optimiert man den Workflow?
6. **Best Practices**: Wie macht man es professionell?

### Aufgabenstruktur
Jede Aufgabe folgt demselben Muster:
- **Frage**: Theoretisches Verständnis prüfen
- **Beispiel**: Konkretes Szenario aus der Praxis
- **Lösung**: Ausführliche Erklärung mit Beispielen
- **Video**: Zusätzliche Erklärung (falls verfügbar)
- **Tipp**: Zusätzlicher Denkanstoß

### Besondere Merkmale
- **Praxisbeispiele**: Jedes Kapitel enthält konkrete Code-Beispiele
- **Vergleiche**: GitHub vs. GitFlow, Rebase vs. Merge, etc.
- **Sicherheit**: Besonderer Fokus auf .gitignore und Secrets Management
- **Teamarbeit**: Collaboration-Workflows und Best Practices
- **CI/CD**: Automatisierung und moderne Entwicklungspraktiken

## Technische Umsetzung

### Verwendete Features
- **MkDocs Material Theme**: Modernes, responsives Design
- **Python Macros**: Interaktive Aufgaben mit `task()` Macro
- **MathJax**: Mathematische Formeln in Aufgaben
- **Mermaid Diagramme**: Visualisierung von Prozessen
- **Custom CSS**: Angepasste Kartendesigns und Admonitions

### Dateistruktur
```
docs/
├── content/          # Kurskapitel
│   ├── 2.md         # Kursübersicht
│   ├── 3.md         # Historische Entwicklung
│   ├── 4.md         # Grundkonzepte
│   ├── 5.md         # Installation
│   ├── 6.md         # Remote-Repositories
│   ├── 7.md         # GitHub/GitLab
│   ├── 8.md         # Projektdateien
│   ├── 9.md         # Fortgeschrittene Features
│   └── 10.md        # Projektadministration
├── assets/          # Bilder und Logo
├── stylesheets/     # Custom CSS
├── javascripts/     # Custom JavaScript
└── index.md         # Hauptseite

tasks/
├── 02_00_01.yaml    # Kursverständnis
├── 03_00_01.yaml    # Historische Entwicklung
├── 04_00_01.yaml    # Grundkonzepte
├── 05_00_01.yaml    # Installation
├── 06_00_01.yaml    # Remote-Repositories
├── 07_00_01.yaml    # GitHub/GitLab
├── 08_00_01.yaml    # Projektdateien
├── 09_00_01.yaml    # Fortgeschrittene Features
└── 10_00_01.yaml    # Projektadministration
```

## Lernziele

Nach Abschluss des Kurses können Teilnehmer:

1. **Verstehen** die historische Entwicklung von Versionskontrolle
2. **Anwenden** grundlegende Git-Befehle für lokale Repository-Verwaltung
3. **Implementieren** effektive Branching-Strategien für Projekte
4. **Verwalten** Projektdateien und Konfigurationsdateien korrekt
5. **Kollaborieren** mit Teams auf Remote-Repositories
6. **Lösen** Konflikte bei paralleler Arbeit mehrerer Entwickler
7. **Automatisieren** Build- und Deployment-Prozesse mit CI/CD
8. **Anwenden** fortgeschrittene Git-Features (Rebase, Stash, etc.)
9. **Implementieren** Best Practices für professionelle Projektadministration

## Zielgruppe

- **Einsteiger**: Keine Vorkenntnisse in Versionskontrolle erforderlich
- **Entwickler**: Grundkenntnisse in Programmierung vorausgesetzt
- **Teams**: Für die Einführung von Git in bestehende Projekte
- **Studenten**: Für akademische Projekte und Abschlussarbeiten

## Materialien

- **Präsentationen**: Folien zu jedem Kapitel
- **Code-Beispiele**: Praktische Übungen und Demonstrationen
- **Aufgaben**: Interaktive Übungen zur Wissensüberprüfung
- **Projekt**: Abschlussprojekt für praktische Anwendung
- **Cheat Sheets**: Zusammenfassungen der wichtigsten Befehle

## Bewertung

- **Teilnahme**: Aktive Mitarbeit in Übungen (40%)
- **Praktische Aufgaben**: Lösung von Aufgaben nach jedem Kapitel (30%)
- **Abschlussprojekt**: Anwendung des Gelernten in einem realen Projekt (30%)

## Zeitplan

| Zeit | Thema | Dauer |
|------|-------|-------|
| **Tag 1** | | |
| 09:00 | Einführung und historischer Hintergrund | 60 min |
| 10:00 | Grundlegende Konzepte und Installation | 60 min |
| 11:00 | Erste Schritte mit Git | 90 min |
| 12:30 | Mittagspause | 60 min |
| 13:30 | Remote-Repositories und Collaboration | 90 min |
| 15:00 | GitHub/GitLab Integration | 90 min |
| 16:30 | Projektdateien und .gitignore | 90 min |
| **Tag 2** | | |
| 09:00 | Fortgeschrittene Git-Features | 90 min |
| 10:30 | Projektadministration und Best Practices | 90 min |
| 12:00 | Abschlussprojekt | 90 min |
| 13:30 | Mittagspause | 60 min |
| 14:30 | Praktische Anwendungen | 90 min |
| 16:00 | Abschluss und Zertifikate | 30 min |

## Ressourcen

- **Offizielle Git-Dokumentation**: https://git-scm.com/doc
- **GitHub Learning Lab**: https://lab.github.com/
- **Git Cheat Sheet**: https://training.github.com/downloads/de/github-git-cheat-sheet/
- **Pro Git Buch**: https://git-scm.com/book/de/v2

## Kontakt

Für Fragen oder Feedback wenden Sie sich bitte an den Kursleiter.

---

*Dieser Kurs wurde mit MkDocs Material erstellt und ist Teil der Basis Wiki.*