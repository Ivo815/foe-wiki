# FoE-Wiki – Projekt-Summary
**Datum:** 2026-09-22  
**Status:** GitHub Pages in Aktivierung

---

## 🎯 Projektziel

Aufbau einer persistenten Wissensbasis für die **swissfuture-Fachgruppe Futures of Education (FoE)**. Die Wiki hält Rohquellen, destillierte Konzepte und laufendes Prozessprotokoll strukturiert und navigierbar.

**Nutzer:** Ivo Veith (ivoogle@gmail.com)  
**Organisation:** swissfuture / Futures of Education  
**GitHub:** Ivo815 (https://github.com/Ivo815/foe-wiki)

---

## 📂 Lokale Verzeichnisstruktur

```
/Users/ivo/Library/Mobile Documents/com~apple~CloudDocs/04_Projekte/SF Futures of Education/SF-Wiki/
├── .git/                           # Git-Repository (initialisiert 2026-09-22)
├── .gitignore                      # Ausschlussregeln für Git
├── CLAUDE.md                       # Projektrichtlinien für KI-Zusammenarbeit
├── README.md                       # Projektuebersicht für GitHub
├── SUMMARY.md                      # Diese Datei
├── index.md                        # Katalog aller Seiten
├── log.md                          # Chronologisches Prozessprotokoll
├── dashboard.html                  # Interaktives HTML-Dashboard (mit Suche/Filter)
│
├── raw/                            # Rohquellen (unverändert)
│   ├── veith-predetermined-elements-260526.txt
│   └── veith-bildungsinhalte-ki-260328.txt
│
└── wiki/
    ├── sources/                    # Zusammenfassungen zu Rohquellen
    │   ├── veith-predetermined-elements-260526.md
    │   └── veith-bildungsinhalte-ki-260328.md
    │
    ├── concepts/                   # Zentrale Konzepte & Begriffe
    │   ├── predetermined-elements.md
    │   ├── scenario-planning.md
    │   ├── swiss-foresight-method.md
    │   ├── curriculum-design.md
    │   └── ai-in-education.md
    │
    ├── theses/                     # Destillierte Erkenntnisse (noch leer)
    │
    └── people/                     # Beiträge einzelner Personen (noch leer)
```

---

## 📚 Wiki-Inhalte (aktuell: 7 Seiten)

### **Quellen (2)**

| Seite | Autor | Datum | Inhalt |
|-------|-------|-------|--------|
| `veith-predetermined-elements-260526.md` | Ivo Veith | Mai 2026 | Predetermined Elements als methodischer Anker für Szenarioplanung mit Schweizer Bezug. 6 Kategorien PE, 3 Funktionen für swissfuture, methodische Caveats. |
| `veith-bildungsinhalte-ki-260328.md` | Ivo Veith | März 2026 | "Nicht nur wie, sondern was" – KI als analytisches Instrument zur Lehrplanentwicklung. Lehrpläne als Sedimentschichten, 3 Analyseebenen (Kohärenz/Wirkung/Komparation), exponentielle Dynamik. |

### **Konzepte (5)**

| Seite | Beschreibung |
|-------|-------------|
| `predetermined-elements.md` | Definition, Abgrenzungen (nicht Prognosen/Trends), methodischer Nutzen, Kategorien, Caveats |
| `scenario-planning.md` | Definition, Wack-Ursprung (1970er), Kernprinzipien, Aufbau, Unterschied zu Prognosen |
| `swiss-foresight-method.md` | 7 Dimensionen der Wegweisung (Plausibilität, Transparenz, Partizipation, Pluralität, Empowerment, Holismus, Neuheit), Operationalisierungsfrage |
| `curriculum-design.md` | Lehrplanentwicklung als epistemisches Problem, Sedimentschichten-Ansatz, Shifts (Inhalt→Fähigkeit, statisch→adaptiv, politisch→analytisch) |
| `ai-in-education.md` | Aktuelle Diskurse vs. Lücke, 3 analytische Analysen, Goodhart's Dilemma, exponentielle Dynamik |

### **Thesen (0)**
Noch keine – sollen destillierte Erkenntnisse aus den Quellen werden (nach 4-Stufen-Gliederung: Analyse → Verdichtung → These → Verifikation)

### **Menschen (0)**
Noch keine – werden bei Bedarf angelegt

---

## 🔄 Frontmatter-Struktur (alle Seiten)

```yaml
---
title: "Seitentitel"
type: these | concept | source | person
visibility: intern | extern
created: YYYY-MM-DD
updated: YYYY-MM-DD
related: [konzept1, konzept2]
---
```

**Wichtig:**
- `visibility: intern` ist Standard (keine Veröffentlichung ohne explizite Freigabe)
- `related:` verbindet Seiten untereinander
- Alle Dates: 2026-09-22 (Initialisierungsdatum)

---

## 🎨 Dashboard (dashboard.html)

**Features:**
- ✅ Interaktive Suche (Volltextsuchfeld)
- ✅ Filter-Buttons (Alle / Quellen / Konzepte)
- ✅ Statistik-Karten (7 Seiten, 2 Quellen, 5 Konzepte, 0 Thesen)
- ✅ Modal-Popups mit Seiten-Inhalten
- ✅ Tastatursteuerung (Escape zum Schliessen)
- ✅ swissfuture-Logo (blau, SVG)

**Lokale URL:** Öffne `dashboard.html` im Browser  
**GitHub Pages URL (in Kürze):** https://ivo815.github.io/foe-wiki/dashboard.html

---

## 📋 Projektrichtlinien (CLAUDE.md)

Die Datei `CLAUDE.md` definiert:

1. **Rollenverständnis:** Claude ist Verwalter der Wiki, nicht Chatbot
2. **Vier-Stufen-Gliederung für Thesen:**
   - Analyse (was Quellen zeigen, ohne Wertung)
   - Verdichtung (zentrale Erkenntnisse)
   - These (klare, prüfbare Position)
   - Verifikation (wie gegenzuprüfen, offene Fragen)

3. **Sieben Bewertungsdimensionen:**
   - Plausibilität, Methodische Transparenz, Partizipation
   - Pluralität, Empowerment, Holismus, Neuheit

4. **Visibility-Regel:** `extern`-Seiten dürfen nicht auf `intern`-Seiten verlinken; keine Selbstreferenzen auf Ivo ohne explizite Anweisung

5. **Quellendisziplin:** Aussagen brauchen belastbare Primärquellen oder werden als Annahmen gekennzeichnet

6. **Prozesse:**
   - **Ingest:** Quelle lesen → Zusammenfassung → betroffene Seiten aktualisieren → index.md aktualisieren → log.md eintrag
   - **Query:** index.md durchsuchen → relevante Seiten → neue Erkenntnisse als Seiten festhalten
   - **Lint:** Widersprüche, verwaiste Seiten, Visibility-Verstösse prüfen

---

## 🔧 Git & GitHub-Setup

### **Git-Konfiguration (lokal)**
```
Repository-Pfad: /Users/ivo/Library/Mobile Documents/com~apple~CloudDocs/04_Projekte/SF Futures of Education/SF-Wiki/
Git-Benutzer: Ivo Veith (ivoogle@gmail.com)
Default-Branch: main
Remote: origin = https://github.com/Ivo815/foe-wiki.git
```

### **GitHub-Repository**
```
URL: https://github.com/Ivo815/foe-wiki
Owner: Ivo815
Visibility: Public
First Commit: bbf0f9c (2026-09-22)
Commit Message: "Initial commit: FoE-Wiki mit 7 Seiten, Dashboard und Dokumentation"
```

### **GitHub Pages** (in Aktivierung)
```
Status: In Konfiguration (Stand: 2026-09-22)
Source: main branch, / (root)
Expected URL: https://ivo815.github.io/foe-wiki/dashboard.html
Estimated Availability: ~2 Minuten nach Aktivierung
```

---

## 📝 Wichtige Dateien im Detail

### **index.md** (Katalog)
- Gruppiert nach `theses/`, `concepts/`, `sources/`, `people/`
- Format: Link, Einzeiler-Zusammenfassung, Visibility-Kennzeichen
- Aktuell: 2 Quellen + 5 Konzepte

### **log.md** (Prozessprotokoll, append-only)
- Format: `[DATUM] [OPERATIONSTYP] Beschreibung`
- Einträge: INIT, INGEST (2x Quelle, 2x Concept-Seite), INDEX
- Sortierung: chronologisch, für `grep`-barkeit

### **CLAUDE.md** (Projektrichtlinien)
- Muss im Wurzelverzeichnis heissen, damit Claude Code es auto-lädt
- Definiert Rollenverständnis, Prozesse, Qualitätsstandards
- Ist nicht zu bearbeiten ohne explizite Freigabe

---

## 🚀 Nächste Schritte (TODO)

| Aktion | Status | Details |
|--------|--------|---------|
| GitHub Pages aktivieren | 🔄 In Progress | Settings → Pages → Source: main/root → Save. URL wird dann: https://ivo815.github.io/foe-wiki/dashboard.html |
| Dashboard testen | ⏳ Pending | Sobald GitHub Pages live ist, dashboard.html öffnen und Suche/Filter testen |
| Team einladen | ⏳ Pending | Collaborators hinzufügen (Settings → Collaborators) |
| Erste Thesen destillieren | ⏳ Pending | Aus den 2 Quellen 2-3 zentrale Thesen nach 4-Stufen-Gliederung |
| Memory System aktivieren | ⏳ Pending | Nutzer-/Feedback-/Projekt-/Referenz-Memories in `/Users/ivo/.claude/projects/.../memory/` |

---

## 💾 Persistenter Kontext (für zukünftige Chats)

**Speicherort für Memory:** `/Users/ivo/.claude/projects/-Users-ivo-Library-Mobile-Documents-com-apple-CloudDocs-04-Projekte-SF-Futures-of-Education-SF-Wiki/memory/`

**Was speichern:**
- Nutzer-Memory: Ivo Veith ist Zukunftsarchitekt bei swissfuture, arbeitet an FoE-Wiki
- Feedback-Memory: Claude soll als Wiki-Verwalter fungieren, nicht als Chatbot
- Projekt-Memory: FoE-Wiki, GitHub Ivo815/foe-wiki, GitHub Pages URL, Inhalt, Richtlinien
- Reference-Memory: CLAUDE.md ist Leitdokument, GitHub-Repository ist Quelle der Wahrheit

---

## 📊 Metriken (2026-09-22)

| Metrik | Wert |
|--------|------|
| Seiten gesamt | 7 |
| Quellen | 2 |
| Konzepte | 5 |
| Thesen | 0 |
| Rohquellen | 2 |
| Commits | 1 |
| Lines of Code/Markdown | ~1.784 |
| Dashboard Features | 5 (Suche, Filter, Modal, Stats, Styling) |
| Git Remote | 1 (GitHub) |

---

## 🔗 Wichtige URLs & Pfade

| Ressource | Ort/URL |
|-----------|---------|
| Lokales Repository | `/Users/ivo/Library/Mobile Documents/com~apple~CloudDocs/04_Projekte/SF Futures of Education/SF-Wiki/` |
| GitHub Repository | https://github.com/Ivo815/foe-wiki |
| GitHub Pages (in Kürze) | https://ivo815.github.io/foe-wiki/dashboard.html |
| Dashboard lokal | Öffne `dashboard.html` im Browser |
| Wiki-Katalog | `index.md` |
| Prozessprotokoll | `log.md` |
| Projektrichtlinien | `CLAUDE.md` |

---

## 👤 Benutzerkontext

**Name:** Ivo Veith  
**Email:** ivoogle@gmail.com  
**GitHub:** Ivo815  
**Rolle:** Zukunftsarchitekt bei swissfuture, Maintainer der FoE-Wiki  
**Erwartungen:** Wiki als lebende Systemdokumentation, strukturiert nach FoE-Logik, transparent und versionskontrolliert

---

## ✅ Abgeschlossene Milestones

- [x] Wiki-Verzeichnisstruktur aufgebaut
- [x] 2 Quellen ingested (Veith Mai 2026 + März 2026)
- [x] 5 Konzept-Seiten erstellt
- [x] Dashboard mit HTML/CSS/JS entwickelt (Suche, Filter, Modal)
- [x] index.md und log.md aktualisiert
- [x] Git-Repository initialisiert
- [x] GitHub-Remote verbunden
- [x] Erster Commit auf GitHub gepusht
- [x] README.md und .gitignore erstellt

---

## ⏳ In Progress

- 🔄 GitHub Pages aktivieren (warte auf Bestätigung)
- 🔄 Dashboard live-testen

---

**Zusammenfassung bereit für nächste Sitzung. Bei Fragen oder Weiterarbeit: Diese Summary als Kontext verwenden.**
