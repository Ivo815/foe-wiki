# FoE-Wiki – Futures of Education

Persistente Wissensbasis der **swissfuture-Fachgruppe Futures of Education (FoE)**.

## 📖 Zugang

**Dashboard (zum Browsen):** https://ivo815.github.io/foe-wiki/dashboard.html

**Rohquellen & Markdown:** [Dieses Repository](https://github.com/Ivo815/foe-wiki)

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
└── dashboard.html               # Interaktive Weboberfläche (liest index.md und wiki/ zur Laufzeit)
```

## 🗂️ Aktueller Stand

Die aktuelle Anzahl und Liste aller Seiten steht in [`index.md`](index.md), oder direkt im [Dashboard](https://ivo815.github.io/foe-wiki/dashboard.html) sichtbar. Wird hier bewusst nicht dupliziert, damit diese README nicht bei jedem Ingest von Hand nachgeführt werden muss.

## 🔄 Mitarbeit

### Für Leser:innen

Öffne das [Dashboard](https://ivo815.github.io/foe-wiki/dashboard.html) im Browser. Keine Installation nötig.

### Für Autor:innen

```
# Repository clonen
git clone https://github.com/Ivo815/foe-wiki.git
cd foe-wiki

# Neue Seite hinzufügen oder bestehende bearbeiten
# ... (siehe CLAUDE.md für Richtlinien)

# Änderungen committen und pushen
git add .
git commit -m "[INGEST] neue Quelle hinzugefügt"
git push
```

Prozess siehe auch: [CLAUDE.md](https://github.com/Ivo815/foe-wiki/blob/main/CLAUDE.md) → Ingest, Query, Lint

## 📋 Richtlinien

- **Frontmatter-Pflicht:** Jede Seite in `wiki/` hat YAML-Metadaten (title, type, visibility, created, updated, related)
- **Vier-Stufen-Gliederung:** Thesen folgen Analyse → Verdichtung → These → Verifikation
- **Sieben Bewertungsdimensionen:** Plausibilität, Transparenz, Partizipation, Pluralität, Empowerment, Holismus, Neuheit
- **Visibility-Regel:** `intern` (Standard) oder `extern` (nach Freigabe)
- **Quellendisziplin:** Aussagen brauchen belastbare Quellen

Siehe [CLAUDE.md](https://github.com/Ivo815/foe-wiki/blob/main/CLAUDE.md) für ausführliche Richtlinien.

## 📝 Protokoll

Alle Vorgänge (Ingest, Query, Lint) werden chronologisch in [log.md](log.md) dokumentiert.

Format: `[DATUM] [OPERATIONSTYP] Beschreibung`

## 👥 Team

**Maintainer:** Ivo Veith

**Fachgruppe:** swissfuture Futures of Education (FoE)

## 📄 Lizenz

Diese Wissensbasis ist intern für swissfuture. Siehe Visibility-Richtlinien für externe Freigaben.
