---
title: Academic Freedom Index – Update 2026
type: source
visibility: intern
created: 2026-11-13
updated: 2026-11-13
related: [wissenschaftsfreiheit]
---

# Academic Freedom Index – Update 2026

**Quelle:** Katrin Kinzelbach, Staffan I. Lindberg, Lars Lott, Angelo Vito Panaro | FAU Erlangen-Nürnberg und V-Dem Institute | 2026 | doi:10.25593/open-fau-2865
**Format:** PDF, 18 Seiten
**Rohquellen-Referenz:** [raw/afi-update-2026.md](../../raw/afi-update-2026.md) (PDF nicht im Repo)

*Written for: FoE-Mitglieder, die den Zustand der Wissenschaftsfreiheit als Rahmenbedingung für Bildung und Forschung einordnen wollen.*

## Zusammenfassung

Der Bericht aktualisiert den Academic Freedom Index (AFI) mit Daten bis Ende 2025. Der Index misst die tatsächliche (de facto) Wissenschaftsfreiheit in 179 Ländern und Territorien auf einer Skala von 0 (vollständig eingeschränkt) bis 1 (vollständig frei). Er beruht auf den Einschätzungen von 2357 Länderexpert:innen, die ein Bayes'sches Messmodell des V-Dem-Projekts zu Indexwerten mit Unsicherheitsintervallen verdichtet.

Die Kernaussage: Zwischen 2015 und 2025 ist die Wissenschaftsfreiheit in 50 Ländern substanziell und statistisch signifikant gesunken, in 9 Ländern gestiegen. Der globale Rückgang beginnt laut Bericht um 2012.

## Was der Bericht zeigt

### Die fünf Indikatoren

| Ebene | Indikator | Länder mit Rückgang 2015–2025 | Länder mit Anstieg |
|---|---|---|---|
| Individuell | Freiheit von Forschung und Lehre | 51 | 13 |
| Individuell | Freiheit des akademischen Austauschs | 47 | 11 |
| Individuell | Freiheit der akademischen und kulturellen Äusserung | 46 | 16 |
| Institutionell | Institutionelle Autonomie | 43 | 11 |
| Institutionell | Campus-Integrität | 51 | 11 |

Alle fünf Dimensionen sinken in mehr Ländern, als sie steigen. Die institutionelle Autonomie ist etwas weniger betroffen als die übrigen.

### Regionale Lage 2025

Besser geschützt ist die Wissenschaftsfreiheit laut Bericht in Lateinamerika, Europa, Nordamerika, Ozeanien und grossen Teilen des südlichen und westlichen Afrika. Schwächer ist sie in Asien sowie im Nahen Osten und Nordafrika. Der bevölkerungsgewichtete Durchschnitt fällt stärker als der Länderdurchschnitt.

### Schwerpunkt institutionelle Autonomie

- Institutionelle Autonomie und Freiheit von Forschung und Lehre korrelieren über 179 Länder im Mittel 2000–2025 stark (Pearson r = 0,91). Der Bericht liest das als Stütze für die These, dass autonome Hochschulen die Freiheit der einzelnen Forschenden schützen. Eine Korrelation belegt diese Wirkungsrichtung nicht für sich allein.
- 43 Länder verzeichnen 2015–2025 einen signifikanten Rückgang der institutionellen Autonomie. In 21 davon war sie 2015 sehr gut geschützt. Genannt werden unter anderem Österreich, Polen, Portugal, die Niederlande, die Slowakei und die **Schweiz**, dazu Kanada, die USA, Argentinien, Bolivien, El Salvador und Peru.
- USA: Die institutionelle Autonomie fällt von 3,3 (2019) auf 1,7 (2025) auf der Ordinalskala 0–4. Der Bericht nennt Massnahmen auf Ebene der Bundesstaaten ab 2020 und Massnahmen der Bundesregierung 2025 als Treiber und vergleicht den Verlauf mit Ungarn, Indien und der Türkei, wo der Rückgang langsamer verlief.
- Gegenbewegung: Gerichtsurteile und Widerstand von Hochschulen und Zivilgesellschaft in den USA. Der Bericht hält ausdrücklich offen, ob der Rückgang gestoppt ist.

### Länderwerte

Abbildungen 8 und 9 zeigen alle Länder mit Punktschätzung und Unsicherheitsintervall, eingeteilt in fünf Statusgruppen A bis E (je ein Fünftel der Skala). Die Schweiz steht 2025 in der Statusgruppe B und ist als signifikanter Rückgang markiert.

## Abgleich mit den Daten (beim Ingest durchgeführt)

Die Länderwerte 2015–2025 wurden aus dem V-Dem-Datensatz v16 gelesen (Variable `v2xca_academ`).

| Prüfpunkt | Ergebnis |
|---|---|
| Anzahl Länder | 179, wie im Bericht |
| 50 Rückgänge, 9 Anstiege (Veränderung ≥ 0,1 und nicht überlappende Intervalle) | Reproduziert |
| Länderdurchschnitt | 0,63 (2015) → 0,55 (2025), passt zu Abb. 3 |
| Bevölkerungsgewichteter Durchschnitt | 0,49 → 0,36. Eigene Berechnung mit Weltbank-Bevölkerungszahlen aus dem V-Dem-Datensatz (171 Länder, 2025 mit Stand 2024). Der Bericht nennt dazu keine Zahl, die Kurve in Abb. 3 passt. |
| Schweiz | 0,93 (2015) → 0,77 (2025) |
| USA | 0,92 (2015) → 0,40 (2025), davon 0,68 → 0,40 von 2024 auf 2025 |
| Deutschland | 0,96 → 0,88 |

## Vorbehalte

- **Expertenurteile:** Der AFI misst Einschätzungen, keine direkt beobachtbaren Grössen. Der Bericht empfiehlt, Vergleiche nur unter Beachtung der Unsicherheitsintervalle zu ziehen. Überlappen die Intervalle zweier Länder, ist keine Rangaussage möglich.
- **Uneinheitliche Zahl im Bericht:** Die Zusammenfassung nennt 50 Länder mit Rückgang, S. 14 spricht von 52 rot markierten Ländern. Fussnote 39 erklärt die Differenz: In Deutschland und Österreich ist der Rückgang statistisch signifikant, aber nicht substanziell.
- **Versionsabhängigkeit:** Werte verschiedener Datensatzversionen sind nicht direkt vergleichbar, weil Expert:innen frühere Jahre nachträglich neu bewerten können. Zahlen aus älteren AFI-Berichten nicht mit diesen mischen.
- **Ursachen:** Die Erklärungen zum Rückgang in den USA stützen sich auf Medienberichte und Stellungnahmen von Verbänden. Sie sind im Repo nicht einzeln geprüft.
- **Nicht gelesen:** Die Projektwebseite war beim Ingest nicht erreichbar. Vom Methodenpapier (V-Dem Working Paper 21) wurden die Seiten 1–20 von 37 gelesen.

## Bezug zur FoE-Arbeit

- Der Bericht ist eine Zustands- und Trendbeschreibung bis 2025, kein Zukunftsbild. Aussagen über die weitere Entwicklung macht er nicht. Wer den Trend in ein Szenario fortschreibt, trifft eine Annahme, die als solche zu kennzeichnen ist.
- Der Rückgang ist nach den Kriterien der FoE kein vorbestimmtes Element: Der Bericht selbst beschreibt Gegenbewegungen und neun Länder mit Verbesserung.
- Eine Bewertung nach den sieben Dimensionen entfällt hier, weil die Quelle kein Zukunftsbild ist.

## Offene Fragen

- Was erklärt den Rückgang in der Schweiz (0,93 → 0,77, vor allem seit 2023)? Der Bericht nennt die Schweiz nur in einer Aufzählung zur institutionellen Autonomie und gibt keine Gründe an.
- Welche der fünf Indikatoren tragen in der Schweiz zum Rückgang bei? Die Indikatorwerte liegen im V-Dem-Datensatz vor und wurden noch nicht ausgewertet.
- Wie verhält sich der AFI zu Indikatoren für das Schulsystem? Der Index erfasst Hochschulen und Forschung, nicht die Volksschule.

## Verweise

- Konzept: [[wissenschaftsfreiheit]] (mit animierter Weltkarte 2015–2025)
