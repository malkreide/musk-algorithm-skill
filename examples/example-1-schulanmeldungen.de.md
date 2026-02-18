# Beispiel: Prozessanalyse Schulanmeldungen

🌐 **Language / Sprache:** [English](example-1-school-enrollment.md) | [Deutsch](example-1-schulanmeldungen.de.md)

## Ausgangslage

Das Schulamt der Stadt ZÃ¼rich erhÃ¤lt jÃ¤hrlich ca. 3'500 Schulanmeldungen fÃ¼r die 1. Klasse. Der aktuelle Prozess umfasst 12 Schritte und dauert durchschnittlich 6 Wochen vom Eingang bis zur BestÃ¤tigung.

**Aktueller Prozess (vereinfacht):**

1. Eltern laden PDF-Formular von Website herunter
2. Eltern fÃ¼llen Formular handschriftlich aus
3. Eltern senden Formular per Post oder scannen es ein und senden per E-Mail
4. Sekretariat empfÃ¤ngt und sortiert Anmeldungen
5. Sekretariat erfasst Daten manuell in Excel
6. Sekretariat leitet Excel an Schulkreis-Koordination weiter
7. Schulkreis-Koordination prÃ¼ft Wohnort-ZustÃ¤ndigkeit
8. Schulkreis-Koordination erstellt Klassenzuteilungs-Vorschlag
9. Schulleitung genehmigt Klassenzuteilung
10. Schulkreis-Koordination erfasst finale Zuteilung in SchulDB
11. Sekretariat erstellt BestÃ¤tigungsbrief (Word-Vorlage)
12. Sekretariat druckt und versendet Brief per Post

**Problem:** Hoher manueller Aufwand, viele MedienbrÃ¼che, lange Wartezeiten.

---

## Analyse nach Musk-Algorithmus

### Schritt 1: Anforderungen hinterfragen

| # | Anforderung | Urheber | Problem das gelÃ¶st wird | Gesetzliche Grundlage? | Bewertung | DatenqualitÃ¤t |
|---|---|---|---|---|---|---|
| 1.1 | PDF-Formular | IT-Abteilung (2012) | "Einheitliches Layout" | Nein | ðŸ”´ | ðŸ”µ Belegt: IT-Doku vorhanden |
| 1.2 | Handschriftliche AusfÃ¼llung | Unbekannt ("schon immer") | Keine klare | Nein | ðŸ”´ | âšª SchÃ¤tzung: Kein Urheber identifiziert |
| 1.3 | Post/E-Mail-Eingang | Datenschutz-Policy (2015) | Vermeidung Cloud-Tools | Ja (DSG ZH) | ðŸŸ¢ | ðŸ”µ Belegt: Rechtsgutachten liegt vor |
| 1.4 | Manuelle Excel-Erfassung | Sekretariat | "Zur Weiterverarbeitung" | Nein | ðŸ”´ | ðŸ”µ Belegt: Prozess dokumentiert |
| 1.5 | Wohnort-PrÃ¼fung | Schulkreis-Koordination | Korrekte Schulzuteilung | Ja (VSG Â§5) | ðŸŸ¢ | ðŸ”µ Belegt: Gesetzestext |
| 1.6 | Klassenzuteilungs-Vorschlag | Schulkreis-Koordination | PÃ¤dagogische Balance | Nein | ðŸŸ¡ | âšª SchÃ¤tzung: Benefit unklar |
| 1.7 | Genehmigung durch Schulleitung | Org-Reglement (2018) | "Vier-Augen-Prinzip" | Nein | ðŸŸ¡ | ðŸ”µ Belegt: Reglement vorhanden |
| 1.8 | Erfassung in SchulDB | IT-Abteilung | Datenhaltung fÃ¼r Schuljahr | Ja (VSM Â§12) | ðŸŸ¢ | ðŸ”µ Belegt: Verordnung |
| 1.9 | Word-Vorlage fÃ¼r Brief | Kommunikation (2010) | "Corporate Design" | Nein | ðŸŸ¡ | ðŸ”µ Belegt: CD-Richtlinie |
| 1.10 | Druck und Postversand | Kommunikation | "Offizieller Charakter" | Nein | ðŸ”´ | âšª SchÃ¤tzung: Keine Dokumentation |

**Erkenntnisse:**
- ðŸŸ¢ **3 valide Anforderungen** (gesetzlich verankert)
- ðŸŸ¡ **3 fragwÃ¼rdige Anforderungen** (interner Ursprung, Nutzen unklar)
- ðŸ”´ **4 LÃ¶schkandidaten** (kein klarer Urheber oder obsolet)

---

### Schritt 2: LÃ¶schen

#### Stakeholder-Analyse

| LÃ¶schkandidat | Betroffene Stakeholder | Art der Betroffenheit | Einbezug erforderlich? | Kommunikationsmassnahme |
|---|---|---|---|---|
| 1.1 PDF-Formular | Eltern, IT | Eltern mÃ¼ssen neues System nutzen | Ja | Information via Newsletter, Website-Update |
| 1.2 Handschriftlich | Eltern | Keine â€“ digitale Eingabe ist einfacher | Nein | - |
| 1.4 Excel-Erfassung | Sekretariat | Arbeitslast reduziert sich | Ja | Schulung fÃ¼r neue LÃ¶sung |
| 1.6 Klassenzuteilungs-Vorschlag | Schulkreis-Koordination | Entscheidungskompetenz verschiebt sich | Ja | Workshop mit Koordination |
| 1.10 Postversand | Eltern, Sekretariat | Eltern erhalten E-Mail statt Brief | Ja | Opt-in fÃ¼r Postversand anbieten |

**Streichungen mit BegrÃ¼ndung:**

- âœ‚ï¸ **PDF-Formular** â†’ Ersetzt durch Online-Formular (direkt in SchulDB)
- âœ‚ï¸ **Handschriftliche AusfÃ¼llung** â†’ Digital ist effizienter und fehlerÃ¤rmer
- âœ‚ï¸ **Manuelle Excel-Erfassung** â†’ Direkte Datenbankerfassung
- âœ‚ï¸ **Postversand** â†’ E-Mail-Versand (Opt-in fÃ¼r Post bleibt als Ausnahme)

**Behalten (mit BegrÃ¼ndung):**

- âœ… **Wohnort-PrÃ¼fung** â€“ Gesetzlich erforderlich
- âœ… **SchulDB-Erfassung** â€“ Gesetzlich erforderlich
- âš ï¸ **Genehmigung Schulleitung** â€“ Behalten, aber Prozess vereinfachen (siehe Schritt 3)

**ReversibilitÃ¤tsplan:**
- PDF-Formular: 1 Woche Reaktivierung mÃ¶glich (liegt archiviert auf Server)
- Excel-Erfassung: Kann jederzeit als Backup reaktiviert werden (Template vorhanden)

---

### Schritt 3: Vereinfachen

#### Vorher-Nachher-Vergleich

| Vorher (12 Schritte) | Nachher (5 Schritte) |
|---|---|
| 1. PDF herunterladen<br>2. Handschriftlich ausfÃ¼llen<br>3. Scannen/Post<br>4. Sekretariat sortiert<br>5. Excel-Erfassung<br>6. Weiterleitung<br>7. Wohnort-PrÃ¼fung<br>8. Klassenzuteilung<br>9. Genehmigung SL<br>10. SchulDB-Erfassung<br>11. Brief erstellen<br>12. Druck/Versand | 1. **Online-Formular ausfÃ¼llen** (mit Adress-AutovervollstÃ¤ndigung)<br>2. **Automatische Wohnort-PrÃ¼fung** (Geo-API)<br>3. **Automatische Klassenzuteilung** (Algorithmus mit SL-Review)<br>4. **Automatische E-Mail-BestÃ¤tigung**<br>5. **(Optional) Schulleitung prÃ¼ft Ausnahmen** |

**Vereinfachungsmassnahmen:**

1. **Medienbruch eliminiert**: Papier â†’ Online-Formular direkt in Datenbank
2. **Rollen konsolidiert**: Sekretariat + Schulkreis-Koordination â†’ System (mit Ausnahme-Handling)
3. **Genehmigungskaskade verkÃ¼rzt**: Schulleitung genehmigt nur noch Ausnahmen (z.B. auswÃ¤rtige Kinder), nicht mehr alle Zuteilungen
4. **Dateneingabe-Redundanz eliminiert**: 1x Eingabe durch Eltern, keine manuelle Nacherfassung

---

### Schritt 4: Beschleunigen

**Wartezeiten-Analyse (Vorher):**

| Schritt | Wartezeit | Grund |
|---|---|---|
| Post-Eingang | 1-3 Tage | Postlaufzeit |
| Sekretariat-Erfassung | 2-5 Tage | Batch-Verarbeitung (wÃ¶chentlich) |
| Schulkreis-PrÃ¼fung | 1-2 Wochen | Wartezeit auf Koordinations-Meeting |
| Schulleitung-Genehmigung | 1 Woche | Wartezeit auf SL-Meeting |
| Brief-Versand | 1-3 Tage | Postlaufzeit |

**Gesamte Durchlaufzeit:** 3-6 Wochen

**Beschleunigungsmassnahmen:**

1. **Parallelisierung**: Wohnort-PrÃ¼fung + Klassenzuteilung passieren automatisch beim Formular-Absenden
2. **Echtzeit-Feedback**: Eltern erhalten sofort BestÃ¤tigung statt nach 6 Wochen
3. **Batch-Elimination**: Keine wÃ¶chentliche Verarbeitung mehr, sondern kontinuierlich
4. **Meeting-Reduktion**: Schulleitung prÃ¼ft nur noch Ausnahmen (asynchron, bei Bedarf)

**Neue Durchlaufzeit:** < 24 Stunden (fÃ¼r StandardfÃ¤lle)

---

### Schritt 5: Automatisieren

**Automatisierungsplan:**

| Schritt | Tool/Technologie | PrioritÃ¤t | Aufwand | BegrÃ¼ndung |
|---|---|---|---|---|
| Online-Formular | Webflow / TypeForm | ðŸŸ¢ Quick Win | 2-3 Tage | Einfach zu implementieren |
| Adress-AutovervollstÃ¤ndigung | Google Places API | ðŸŸ¡ Strategisch | 1 Woche | Reduziert Tippfehler |
| Wohnort-PrÃ¼fung (Geo) | OpenStreetMap API | ðŸŸ¢ Quick Win | 3-5 Tage | Eliminiert manuelle PrÃ¼fung |
| Klassenzuteilungs-Algorithmus | Python-Script (KlassenkapazitÃ¤t + Geo) | ðŸŸ¡ Strategisch | 2-3 Wochen | Komplex, aber hoher Nutzen |
| E-Mail-BestÃ¤tigung | SendGrid / Postmark | ðŸŸ¢ Quick Win | 1 Tag | Standard-Integration |
| SchulDB-Anbindung | API-Integration | ðŸŸ¡ Strategisch | 2-4 Wochen | AbhÃ¤ngig von DB-Architektur |

**Warnung:** Klassenzuteilungs-Algorithmus erst automatisieren, nachdem der manuelle Prozess 1 Schuljahr lang stabil gelaufen ist (Schritt-5-Regel).

---

### Zusammenfassung

**Erwartete Wirkung:**

- **Zeitersparnis (Sekretariat):** ~80% (von 40h/Jahr auf 8h/Jahr fÃ¼r Ausnahmen)
- **Zeitersparnis (Eltern):** 6 Wochen Wartezeit â†’ 24h
- **Fehlerreduktion:** ~90% (keine manuelle Dateneingabe mehr)
- **Kostenreduktion:** ~CHF 12'000/Jahr (Druck, Porto, Arbeitszeit)

**Risiken:**

- Technisches Risiko: Ausfall des Online-Formulars â†’ LÃ¶sung: PDF-Backup bleibt verfÃ¼gbar
- Akzeptanzrisiko: Eltern ohne Internet-Zugang â†’ LÃ¶sung: Opt-in fÃ¼r Papier-Anmeldung

---

### Quick-Win-Matrix

```
                      Hohe Wirkung
       â”Œâ”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¬â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”
       â”‚  STRATEGISCH       â”‚   QUICK WINS       â”‚
       â”‚                    â”‚                    â”‚
       â”‚  â€¢ Klassenzuteilungâ”‚  â€¢ Online-Formular â”‚
       â”‚    -Algorithmus    â”‚  â€¢ E-Mail-Versand  â”‚
       â”‚  â€¢ SchulDB-        â”‚  â€¢ Geo-PrÃ¼fung     â”‚
       â”‚    Integration     â”‚                    â”‚
Hoher â”€â”¼â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¼â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”¼â”€ Niedriger
Aufwandâ”‚  VERMEIDEN         â”‚   MITNEHMEN        â”‚  Aufwand
       â”‚                    â”‚                    â”‚
       â”‚  â€¢ Umfassende      â”‚  â€¢ Adress-         â”‚
       â”‚    Prozess-        â”‚    Autovervoll-    â”‚
       â”‚    Neugestaltung   â”‚    stÃ¤ndigung      â”‚
       â”‚                    â”‚                    â”‚
       â””â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”´â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”€â”˜
                      Niedrige Wirkung
```

**Empfohlene Umsetzungsreihenfolge:**

1. **Sofort (1-2 Wochen):** Online-Formular + E-Mail-BestÃ¤tigung + Geo-PrÃ¼fung
2. **Mittel (3-6 Monate):** SchulDB-Integration + Adress-AutovervollstÃ¤ndigung
3. **Langfristig (1-2 Jahre):** Klassenzuteilungs-Algorithmus (erst nach BewÃ¤hrung des manuellen Prozesses)

---

**NÃ¤chste Schritte:**

1. GL-Entscheid: Freigabe fÃ¼r Quick-Wins (Budget: ~CHF 5'000 fÃ¼r Webflow + APIs)
2. Stakeholder-Information: Newsletter an Eltern (Februar 2026)
3. Pilot: 1 Schulkreis testet neuen Prozess (MÃ¤rz 2026)
4. Rollout: Alle Schulkreise (Schuljahr 2026/27)
