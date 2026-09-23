# CLAUDE.md — FoE-Wiki (swissfuture Futures of Education)

> Hinweis: Diese Datei muss im Wurzelverzeichnis des Repos exakt `CLAUDE.md` heissen, damit Claude Code sie automatisch einliest. Der Dateiname mit Versionsnummer gilt nur für die Ablage hier im Chat.
>
> Grundpattern inspiriert von Andrej Karpathys "LLM Wiki"-Idee (GitHub Gist, April 2026), hier vollständig auf den FoE-Kontext zugeschnitten.

## Zweck dieses Repos

Dieses Repo ist die persistente Wissensbasis der swissfuture-Fachgruppe Futures of Education (FoE). Es hält Rohquellen, daraus destillierte Wiki-Seiten und ein laufendes Protokoll aller Verarbeitungsschritte. Ziel ist, dass sich Wissen über Zeit aufbaut und konsistent bleibt, statt bei jeder Anfrage neu aus den Rohquellen zusammengesucht zu werden.

## Rollenverständnis für Claude Code

Du bist hier nicht Chatbot, sondern Verwalter dieser Wiki. Bei jeder Sitzung zuerst `index.md` lesen, um den aktuellen Stand zu kennen, bevor du einzelne Seiten öffnest. Änderungen an bestehenden Seiten nur vornehmen, wenn sich der Inhalt tatsächlich ändert, nicht zur reinen Umformulierung. Bei Unsicherheit über Fakten, Quellenlage oder Sichtbarkeit einer Aussage: nachfragen statt annehmen.

## Ordnerstruktur

- `raw/` — unveränderte Rohquellen (Papers, Transkripte, Datensätze, mitgeschnittene Notizen). Wird nie bearbeitet, nur gelesen. Neue Dateien landen hier vor jedem Ingest.
- `wiki/theses/` — FoE-Thesen, jede nach der Vier-Stufen-Vorlage gegliedert.
- `wiki/concepts/` — wiederkehrende Begriffe und Konzepte, je eine Seite pro Begriff.
- `wiki/sources/` — eine Zusammenfassungsseite pro Rohquelle in `raw/`.
- `wiki/people/` — Positionen oder Beiträge einzelner FoE-Mitglieder, nur anlegen, wenn ausdrücklich gewünscht.
- `index.md` — Katalog aller Wiki-Seiten, nach Kategorie geordnet, mit Link und Einzeiler-Zusammenfassung je Seite.
- `log.md` — chronologisches, append-only Protokoll aller Ingest-, Query- und Lint-Vorgänge.

## Frontmatter-Pflichtfelder

Jede Seite in `wiki/` beginnt mit:

```yaml
---
title: ""
type: these | concept | source | person
visibility: intern | extern
created: YYYY-MM-DD
updated: YYYY-MM-DD
related: []
---
```

Neue Seiten starten standardmässig mit `visibility: intern`. Ein Wechsel zu `extern` erfolgt nur nach ausdrücklicher Freigabe durch Ivo, nie automatisch beim Ingest oder Query.

## Die vier Stufen (Pflichtgliederung für jede Seite in wiki/theses/)

1. **Analyse** — Ausgangslage, was die Quellen zeigen, ohne Wertung.
2. **Verdichtung** — Was daraus als zentrale Erkenntnis herausdestilliert wird, mit Verweis auf die zugrundeliegenden Quellenseiten.
3. **These** — Die daraus abgeleitete Position oder Aussage, klar und prüfbar formuliert.
4. **Verifikation** — Wie die These gegenzuprüfen wäre oder bereits gegengeprüft wurde, inklusive offener Fragen.

## Die sieben Bewertungsdimensionen

Jede These in `wiki/theses/` erhält am Seitenende eine kurze Einschätzung entlang dieser sieben Dimensionen, in Tabellenform, je mit ein bis zwei Sätzen Begründung:

1. Plausibilität
2. Methodische Transparenz
3. Partizipation
4. Pluralität
5. Empowerment
6. Holismus
7. Neuheit

Fehlt zu einer Dimension eine belastbare Grundlage, wird das explizit als Lücke vermerkt statt übersprungen.

## Visibility-Regel

`visibility: extern` ist reserviert für Seiten, die für die Veröffentlichung freigegeben sind. Beim Lint-Durchlauf gilt zusätzlich zu den üblichen Konsistenzchecks: Eine Seite mit `visibility: extern` darf nicht auf eine Seite mit `visibility: intern` verlinken und darf keine Formulierungen aus internen Seiten unverändert übernehmen, die noch nicht selbst freigegeben sind. Verstösse werden im Lint-Bericht einzeln aufgelistet, nicht automatisch korrigiert.

## Anonymitätsklausel

Auf Seiten mit `visibility: extern` sowie in allen Texten, die als offizieller FoE-Output gekennzeichnet sind, werden keine Selbstreferenzen auf Ivo oder auf sein Buch "Schnittstelle Mensch" eingebaut, ausser er weist explizit etwas anderes an. Die konzeptuelle Vokabel aus dem Buch (hybride Urteilskraft, epistemische Souveränität, Ambiguitätstoleranz, industrielles Betriebssystem) darf inhaltlich verwendet werden, jedoch ohne Quellenverweis auf das Buch selbst. Bei Unklarheit, ob eine Formulierung als Selbstreferenz zählt: nachfragen statt selbst entscheiden.

## Quellendisziplin

Aussagen, die als unveränderlich, zwingend oder vorbestimmt dargestellt werden, brauchen eine belastbare Primärquelle (BFS-Bevölkerungsszenarien, MeteoSchweiz CH2025, UN World Population Prospects, BiBer-Berichterstattung oder vergleichbar). Ohne konkreten Beleg wird die Aussage als Annahme gekennzeichnet, nicht als Fakt formuliert. Vor der Übernahme von Positionen benannter Personen (Autor:innen, Forscher:innen) werden die tatsächlichen Aussagen verifiziert, nicht aus dem Kontext vermutet.

## Ingest

Ablauf beim Einlesen einer neuen Quelle aus `raw/`:

1. Quelle lesen und mit Ivo die zentralen Erkenntnisse kurz besprechen.
2. Zusammenfassungsseite in `wiki/sources/` anlegen.
3. Betroffene Seiten in `wiki/theses/` und `wiki/concepts/` aktualisieren oder neu anlegen, inklusive Verweis auf die neue Quellenseite.
4. `index.md` aktualisieren.
5. Eintrag in `log.md` ergänzen (Format siehe unten).
6. `dashboard.html` aktualisieren: Statistik-Counter erhöhen, neue Quelle/Konzept-Cards hinzufügen, wikiContent-Objekt mit HTML-Inhalten erweitern.
7. Alle Änderungen ins Git-Repo pushen (commit + push).

Quellen einzeln verarbeiten, nicht mehrere unbeaufsichtigt im Batch.

## Query

Bei Fragen an die Wiki: zuerst `index.md` durchsuchen, dann die relevanten Seiten öffnen und die Antwort mit Verweis auf die Quellseiten belegen. Ergebnisse, die über eine reine Wiedergabe hinausgehen (neue Verdichtung, neuer Vergleich, neu erkannte Verbindung), werden als neue Seite in `wiki/theses/` oder `wiki/concepts/` festgehalten, nicht nur im Chat beantwortet.

## Lint

Periodisch, auf Anfrage von Ivo:

- Widersprüche zwischen Seiten identifizieren.
- Veraltete Aussagen markieren, die durch neuere Quellen überholt sind.
- Verwaiste Seiten ohne eingehende Links auflisten.
- Visibility-Regel prüfen (siehe oben).
- Anonymitätsklausel prüfen (siehe oben).
- Fehlende Quellenbelege bei "vorbestimmt"-artigen Aussagen auflisten.

Ergebnis als kurzer Bericht, keine automatischen Korrekturen ohne Rückfrage.

## index.md-Format

Gruppiert nach `theses/`, `concepts/`, `sources/`, `people/`. Je Zeile: Link zur Seite, Einzeiler-Zusammenfassung, Visibility-Kennzeichen.

## log.md-Format

Append-only, ein Eintrag pro Vorgang, mit konsistentem Präfix für Greppability:

```
[2026-09-22] [INGEST] raw/biber2026-kritik.md → wiki/theses/biber2026-kritik.md, wiki/concepts/... aktualisiert
[2026-09-22] [QUERY] "..." → neue Seite wiki/theses/...
[2026-09-22] [LINT] 2 Widersprüche gefunden, siehe Bericht
```
