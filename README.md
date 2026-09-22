# FoE-Wiki – Futures of Education

Persistente Wissensbasis der **swissfuture-Fachgruppe Futures of Education (FoE)**.

## 📖 Zugang

**Dashboard (zum Browsen):** https://swissfuture.github.io/foe-wiki/dashboard.html

**Rohquellen & Markdown:** [Dieses Repository](https://github.com/swissfuture/foe-wiki)

## 📂 Struktur

```
foe-wiki/
├── raw/                          # Rohquellen (unverändert)
├── wiki/
│   ├── sources/                 # Zusammenfassungen zu Rohquellen
│   ├── concepts/                # Zentrale Konzepte & Begriffe
│   ├── theses/                  # Destillierte Erkenntnisse
│   └── people/                  # Beiträge einzelner Personen
├── index.md                     # Katalog aller Seiten
├── log.md                       # Chronologisches Prozessprotokoll
├── CLAUDE.md                    # Projektrichtlinien für KI-Arbeit
└── dashboard.html               # Interaktive Weboberfläche
```

## 🗂️ Seiten (aktuell)

### Quellen (2)
- [Ivo Veith – Predetermined Elements als methodischer Anker](wiki/sources/veith-predetermined-elements-260526.md) (Mai 2026)
- [Ivo Veith – Nicht nur wie, sondern was](wiki/sources/veith-bildungsinhalte-ki-260328.md) (März 2026)

### Konzepte (5)
- Predetermined Elements
- Szenarioplanung
- Swissfuture-Methode für belastbare Zukünfte
- Lehrplanentwicklung (Curriculum Design)
- KI in der Bildung

### Thesen (0)
*(Zu erstellen aus destillierten Erkenntnissen)*

## 🔄 Mitarbeit

### Für Leser:innen
Öffne das [Dashboard](https://swissfuture.github.io/foe-wiki/dashboard.html) im Browser. Keine Installation nötig.

### Für Autoren:innen
```bash
# Repository clonen
git clone https://github.com/swissfuture/foe-wiki.git
cd foe-wiki

# Neue Seite hinzufügen oder bestehende bearbeiten
# ... (siehe CLAUDE.md für Richtlinien)

# Änderungen committen und pushen
git add .
git commit -m "[INGEST] neue Quelle hinzugefügt" 
git push
```

Prozess siehe auch: [CLAUDE.md](CLAUDE.md) → Ingest, Query, Lint

## 📋 Richtlinien

- **Frontmatter-Pflicht:** Jede Seite in `wiki/` hat YAML-Metadaten (title, type, visibility, created, updated, related)
- **Vier-Stufen-Gliederung:** Thesen folgen Analyse → Verdichtung → These → Verifikation
- **Sieben Bewertungsdimensionen:** Plausibilität, Transparenz, Partizipation, Pluralität, Empowerment, Holismus, Neuheit
- **Visibility-Regel:** `intern` (Standard) oder `extern` (nach Freigabe)
- **Quellendisziplin:** Aussagen brauchen belastbare Quellen

Siehe [CLAUDE.md](CLAUDE.md) für ausführliche Richtlinien.

## 📝 Protokoll

Alle Vorgänge (Ingest, Query, Lint) werden chronologisch in [log.md](log.md) dokumentiert.

Format: `[DATUM] [OPERATIONSTYP] Beschreibung`

## 👥 Team

**Maintainer:** Ivo Veith (@ivoogleVeith)

**Fachgruppe:** swissfuture Futures of Education (FoE)

## 📄 Lizenz

Diese Wissensbasis ist intern für swissfuture. Siehe Visibility-Richtlinien für externe Freigaben.

---

**Zuletzt aktualisiert:** 2026-09-22
